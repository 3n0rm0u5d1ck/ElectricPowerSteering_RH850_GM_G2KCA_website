---
layout: default
title: HwTq2Meas_MDD
nav_order: 2
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For**

**HandWheel Torque 2 Measurement**

**June 02, 2016Mar 31, 2016**

**Prepared For:**

**Software Engineering**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Prepared By:**

**Krishna Anne,**

**Nexteer Automotive,**

**<u>Saginaw, MI, USAChange</u>** History

|                                           |                    |             |             |
|-------------------------------------|----------------|---------|-----------|
| **Description**                           | **Author**         | **Version** | **Date**    |
| Initial Version                           | Rijvi Ahmed        | 1.0         | 12-Aug-2015 |
| Updated for CM680A_HwTq1Meas_Design_1.2.0 | Selva Sengottaiyan | 2.0         | 14-Oct-2015 |
| Updated for CM680A_HwTq1Meas_Design_1.3.0 | Selva Sengottaiyan | 3.0         | 22-Dec-15   |
| Updated for CM680A_HwTq1Meas_Design_2.0.0 | Krishna Anne       | 4.0         | 31-Mar-16   |
| Updated for CM680A_HwTq1Meas_Design_2.0.1 | Krishna Anne       | 5.0         | 02-Jun-16   |

<u>Table of Contents</u>

[1 Introduction 5](#introduction)

[1.1 Purpose 5](#purpose)

[2 HwTq2Meas & High-Level Description
6](#hwtq2meas-high-level-description)

[3 Design details of software module
7](#design-details-of-software-module)

[3.1 Graphical representation of HwTq2Meas
7](#graphical-representation-of-hwtq2meas)

[3.2 Data Flow Diagram 7](#data-flow-diagram)

[3.2.1 Component level DFD 7](#component-level-dfd)

[3.2.2 Function level DFD 7](#function-level-dfd)

[4 Constant Data Dictionary 8](#constant-data-dictionary)

[4.1 Program (fixed) Constants 8](#program-fixed-constants)

[4.1.1 Embedded Constants 8](#embedded-constants)

[5 Software Component Implementation
9](#software-component-implementation)

[5.1 Sub-Module Functions 9](#sub-module-functions)

[5.1.1 Init: HwTq2MeasInit1 9](#init-hwtq2measinit1)

[5.1.1.1 Design Rationale 9](#design-rationale)

[5.1.1.2 Module Outputs 9](#module-outputs)

[5.1.2 Per: HwTq2MeasPer1 9](#per-hwtq2measper1)

[5.1.2.1 Design Rationale 9](#design-rationale-1)

[5.1.2.2 Store Module Inputs to Local copies
9](#store-module-inputs-to-local-copies)

[5.1.2.3 (Processing of function)……… 9](#processing-of-function)

[5.1.2.4 Store Local copy of outputs into Module Outputs
9](#store-local-copy-of-outputs-into-module-outputs)

[5.1.3 Per: HwTq2MeasPer2 9](#per-hwtq2measper2)

[5.1.3.1 Design Rationale 9](#design-rationale-2)

[5.1.3.2 Store Module Inputs to Local copies
10](#store-module-inputs-to-local-copies-1)

[5.1.3.3 (Processing of function)……… 10](#processing-of-function-1)

[5.1.3.4 Store Local copy of outputs into Module Outputs
10](#store-local-copy-of-outputs-into-module-outputs-1)

[5.2 Server Runables 10](#server-runables)

[5.2.1 HwTq2MeasHwTq2AutTrim_oper 10](#hwtq2meashwtq2auttrim_oper)

[5.2.1.1 Design Rationale 10](#design-rationale-3)

[5.2.1.2 (Processing of function)……… 10](#processing-of-function-2)

[5.2.2 HwTq2MeasHwTq2ClrTrim_Oper 10](#hwtq2meashwtq2clrtrim_oper)

[5.2.2.1 Design Rationale 10](#design-rationale-4)

[5.2.2.2 (Processing of function)……… 10](#processing-of-function-3)

[5.2.3 HwTq2MeasHwTq2ReadTrim_Oper 10](#hwtq2meashwtq2readtrim_oper)

[5.2.3.1 Design Rationale 10](#design-rationale-5)

[5.2.3.2 (Processing of function)……… 10](#processing-of-function-4)

[5.2.4 HwTq2MeasHwTq2TrimPrfmdSts_Oper
11](#hwtq2meashwtq2trimprfmdsts_oper)

[5.2.4.1 Design Rationale 11](#design-rationale-6)

[5.2.4.2 (Processing of function)……… 11](#processing-of-function-5)

[5.2.5 HwTq2MeasHwTq2WrTrim_Oper 11](#hwtq2meashwtq2wrtrim_oper)

[5.2.5.1 Design Rationale 11](#design-rationale-7)

[5.2.5.2 (Processing of function)……… 11](#processing-of-function-6)

[5.2.6 HwTq2MeasTrigStrt_Oper 11](#hwtq2meastrigstrt_oper)

[5.2.6.1 Design Rationale 11](#design-rationale-8)

[5.2.6.2 (Processing of function)……… 11](#processing-of-function-7)

[5.3 Interrupt Functions 11](#interrupt-functions)

[5.4 Module Internal (Local) Functions
11](#module-internal-local-functions)

[5.4.1 Local Function \#1 11](#local-function-1)

[5.4.1.1 Design Rationale 11](#design-rationale-9)

[5.4.2 Local Function \#2 12](#local-function-2)

[5.4.2.1 Design Rationale 12](#design-rationale-10)

[5.5 GLOBAL Function/Macro Definitions
12](#global-functionmacro-definitions)

[6 Known Limitations with Design 13](#known-limitations-with-design)

[7 UNIT TEST CONSIDERATION 14](#unit-test-consideration)

[Appendix A Abbreviations and Acronyms 15](#abbreviations-and-acronyms)

[Appendix B Glossary 16](#glossary)

# Introduction

## Purpose

Module design document for Hand Wheel Torque 2 Measurement Function.

#  HwTq2Meas & High-Level Description

This module configures and processes the RSENT3 peripheral, which is
connected to the handwheel torque 2 sensor. The module configures the
peripheral, triggers transfers, and processes the received data.

# Design details of software module

## Graphical representation of HwTq2Meas

<img
src="ElectricPowerSteering_RH850_GM_G2KCA_website/docs/CM680A_HwTq2Meas_Impl/doc/mediax/media/image1.png"
style="width:4.82222in;height:3.93681in" />

## Data Flow Diagram

### Component level DFD

N/A

### Function level DFD

N/A

# Constant Data Dictionary

## Program (fixed) Constants

### Embedded Constants

#### Local Constants

|                            |            |       |              |
|----------------------------|------------|-------|--------------|
| Constant Name              | Resolution | Units | Value        |
| TQDATAMASK_CNT_U32         | 1          | Cnt   | 0x00000FFFUL |
| SENTSYNCTRIG_CNT_U32       | 1          | Cnt   | 16UL         |
| REGCFGWAITTI_CNT_U32       | 1          | Cnt   | 2UL          |
| FRSMASK_CNT_U32            | 1          | Cnt   | 0x00000001UL |
| CSMASK_CNT_U32             | 1          | Cnt   | 0x000000FEUL |
| FCCNMASK_CNT_U32           | 1          | Cnt   | 0x30000000UL |
| SLOWNEWMSGDATAMASK_CNT_U32 | 1          | Cnt   | 0x80000000UL |
| SLOWCSMASK_ULS_U32         | 1          | Cnt   | 0x00000700UL |
| SLOWMSGIDMASK_CNT_U32      | 1          | Cnt   | 0x00000F00UL |
| SLOWMSGDATAMASK_CNT_U32    | 1          | Cnt   | 0x000000FFUL |
| GEARIDN1MIN_CNT_U08        | 1          | Cnt   | 0U           |
| GEARIDN1MAX_CNT_U08        | 1          | Cnt   | 63U          |

# Software Component Implementation

## Sub-Module Functions

The sub-module functions are grouped based on similar functionality that
needs to be executed in a given “State” of the system (refer States and
Modes). For a given module, the MDD will identify the type and number of
sub-modules required. The sub-module types are described below.

## Init: HwTq2MeasInit1

## Design Rationale

Magic numbers are used due to the large number of numeric values (for
peripheral register configuration), it is more readable and easier to
maintain without using embedded constants for these values. The values
are shown in code comments, and line up exactly with the definitions
given in the design module (a special spreadsheet was included in the
design for this purpose).

See CM680A_HwTq2Meas_RSENTPeripheralCfg.xlsx in design module.

## Module Outputs

*Refer to FDD*

###  [section]

## Per: HwTq2MeasPer1

## Design Rationale

*None*

## Store Module Inputs to Local copies

*Refer to FDD*

## (Processing of function)………

*Refer to FDD*

## Store Local copy of outputs into Module Outputs

*Refer to FDD*

## Per: HwTq2MeasPer2

## Design Rationale

*None*

## Store Module Inputs to Local copies

*Refer to FDD*

## (Processing of function)………

*Refer to FDD*

## Store Local copy of outputs into Module Outputs

*Refer to FDD*

## Server Runables 

## HwTq2MeasHwTq2AutTrim_oper

## Design Rationale

*None*

##  (Processing of function)………

*See block “*HwTq2MeasHwTq2AutTrim*” in the Simulink model of the
design.*

## HwTq2MeasHwTq2ClrTrim_Oper

## Design Rationale

*None*

##  (Processing of function)………

*See block “*HwTq2MeasHwTq2ClrTrim*” in the Simulink model of the
design.*

## HwTq2MeasHwTq2ReadTrim_Oper

## Design Rationale

*None*

##  (Processing of function)………

*See block “HwTq2MeasHwTq2ReadTrim” in the Simulink model of the
design.*

## HwTq2MeasHwTq2TrimPrfmdSts_Oper

## Design Rationale

*None*

##  (Processing of function)………

*See block “HwTq2MeasHwTq2TrimPrfmdSts” in the Simulink model of the
design.*

## HwTq2MeasHwTq2WrTrim_Oper

## Design Rationale

*None*

##  (Processing of function)………

*See block “HwTq2MeasHwTq2WrTrim” in the Simulink model of the design.*

### HwTq2MeasTrigStrt_Oper

## Design Rationale

*None*

##  (Processing of function)………

*See block “HwTq2MeasTrigStrt” in the Simulink model of the design.*

## Interrupt Functions

*None*

## Module Internal (Local) Functions

## Local Function \#1

|                      |                             |      |     |     |
|----------------------|-----------------------------|------|-----|-----|
| **Function Name**    | ReadRegister                | Type | Min | Max |
| **Arguments Passed** | RegisterDummyRead_Cnt_T_u32 | N/A  | N/A | N/A |
| **Return Value**     | RegisterDummyRead_Cnt_T_u32 | N/A  | N/A | N/A |

## Design Rationale

This function can be used both for read-and-use and for read-and-discard

## Local Function \#2

|                      |                           |        |              |              |
|--------------|-----------------------------|----------|----------|----------|
| **Function Name**    | SlowSerlDataRead          | Type   | Min          | Max          |
| **Arguments Passed** | SlowSerlSND_Cnt_T_u32     | uint32 | 0x00000000UL | 0x80000000UL |
| **Arguments Passed** | SlowSerlCS_Cnt_T_u32      | uint32 | 0x00000000UL | 0x00000700UL |
| **Arguments Passed** | SlowSerlMsgID_Cnt_T_u08   | uint8  | 0x00000000UL | 0x00000F00UL |
| **Arguments Passed** | SlowSerlMsgData_Cnt_T_u08 | uint8  | 0x00000000UL | 0x000000FFUL |
| **Return Value**     | None                      | NA     | NA           | NA           |

## Design Rationale

This function is split from SlowSerlDataRead block of Per1 to deal with
cyclomatic complexity.

## GLOBAL Function/Macro Definitions

None

# Known Limitations with Design

None

# UNIT TEST CONSIDERATION

Overflow for the variables **Rte_Pim_HwTq2MeasPrevRollgCntr,
Rte_Pim_HwTq2MsgMissRxCnt, Rte_Pim_HwTq2ComStsErrCntr,
Rte_Pim_HwTq2IntSnsrErrCntr** are intentional as these are used as
rolling counters.

####### Abbreviations and Acronyms

| **Abbreviation or Acronym** | **Description**           |
|-----------------------------|---------------------------|
| DFD                         | Design functional diagram |
| MDD                         | Module design Document    |

####### Glossary

**Note**: Terms and definitions from the source “Nexteer Automotive”
take precedence over all other definitions of the same term. Terms and
definitions from the source “Nexteer Automotive” are formulated from
multiple sources, including the following:

-   ISO 9000

-   ISO/IEC 12207

-   ISO/IEC 15504

-   Automotive SPICE® Process Reference Model (PRM)

-   Automotive SPICE® Process Assessment Model (PAM)

-   ISO/IEC 15288

-   ISO 26262

-   IEEE Standards

-   SWEBOK

-   PMBOK

-   Existing Nexteer Automotive documentation

| **Term** | **Definition**         | **Source** |
|----------|------------------------|------------|
| MDD      | Module Design Document |            |
| DFD      | Data Flow Diagram      |            |

References

| **Ref. \#** | **Title**                                                                                                                                                             | **Version**                    |
|-------|-------------------------------------------------|-----------------|
| 1           | AUTOSAR Specification of Memory Mapping (Link:[AUTOSAR_SWS_MemoryMapping.pdf](http://www.autosar.org/download/R4.0/AUTOSAR_SWS_MemoryMapping.pdf))                    | v1.3.0 R4.0 Rev 2              |
| 2           | MDD Guideline                                                                                                                                                         | EA4 01.00.00                   |
| 3           | [Software Naming Conventions.doc](http://misagweb01.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_fc55f/Software%20Naming%20Conventions%2003x(In%20Work).doc)   | 1.0                            |
| 4           | [Software Design and Coding Standards.doc](http://eroom1.nexteer.com/eRoomReq/Files/erooms8/NextGeneration/0_1a67a9/Software%20Design%20and%20Coding%20Standards.doc) | 2.0                            |
| 5           | FDD – CM680A HwTq2Meas                                                                                                                                                | See Synergy subproject version |

{% endraw %}