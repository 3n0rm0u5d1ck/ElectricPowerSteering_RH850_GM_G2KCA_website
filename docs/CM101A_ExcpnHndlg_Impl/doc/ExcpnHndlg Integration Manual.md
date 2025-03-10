---
layout: default
title: ExcpnHndlg Integration Manual
nav_order: 1
parent: Component Implementation
---
{% raw %}
**Integration Manual**

**For**

**ExcpnHndlg**

**VERSION: 1**

**DATE: 01/19/16**

**Prepared By:**

**Software Group,**

**Nexteer Automotive,**

**Saginaw, MI, USA**

**Location:** The official version of this document is stored in the
Nexteer Configuration Management System.

**Revision History**

|             |                 |                |             |          |
|-------------|-----------------|----------------|-------------|----------|
| **Sl. No.** | **Description** | **Author**     | **Version** | **Date** |
| 1           | Initial version | Lucas Wendling | 1.0         | 01/19/16 |

Table of Contents

[1 Abbrevations And Acronyms 4](#abbrevations-and-acronyms)

[2 References 5](#references)

[3 Dependencies 6](#dependencies)

[3.1 SWCs 6](#swcs)

[3.2 Global Functions(Non RTE) to be provided to Integration Project
6](#global-functionsnon-rte-to-be-provided-to-integration-project)

[4 Configuration REQUIREMeNTS 7](#configuration-requirements)

[4.1 Build Time Config 7](#build-time-config)

[4.2 Configuration Files to be provided by Integration Project
7](#configuration-files-to-be-provided-by-integration-project)

[4.3 Da Vinci Parameter Configuration Changes
7](#da-vinci-parameter-configuration-changes)

[4.4 DaVinci Interrupt Configuration Changes
7](#__RefHeading___Toc440984623)

[4.5 Manual Configuration Changes 7](#manual-configuration-changes)

[5 Integration DATAFLOW REQUIREMENTS
8](#integration-dataflow-requirements)

[5.1 Required Global Data Inputs 8](#required-global-data-inputs)

[5.2 Required Global Data Outputs 8](#required-global-data-outputs)

[5.3 Specific Include Path present 8](#specific-include-path-present)

[6 Runnable Scheduling 9](#runnable-scheduling)

[7 Memory Map REQUIREMENTS 10](#memory-map-requirements)

[7.1 Mapping 10](#mapping)

[7.2 Usage 10](#usage)

[7.3 NvM Blocks 10](#nvm-blocks)

[8 Compiler Settings 11](#compiler-settings)

[8.1 Preprocessor MACRO 11](#preprocessor-macro)

[8.2 Optimization Settings 11](#optimization-settings)

[9 Appendix 12](#appendix)

# Abbrevations And Acronyms

|                  |                 |
|------------------|-----------------|
| **Abbreviation** | **Description** |
|                  |                 |
|                  |                 |
|                  |                 |

# References

This section lists the title & version of all the documents that are
referred for development of this document

|             |           |             |
|-------------|-----------|-------------|
| **Sr. No.** | **Title** | **Version** |
|             |           |             |

# Dependencies

## SWCs

|            |                      |
|------------|----------------------|
| **Module** | **Required Feature** |
|            |                      |

Note : Referencing the external components should be avoided in most
cases. Only in unavoidable circumstance external components should be
referred. Developer should track the references.

## Global Functions(Non RTE) to be provided to Integration Project

SetMcuDiagcIdnData – Non-Rte Server Interface (called as needed)

GetMcuDiagcIdnData – Non-Rte Server Interface (called as needed)

SysErrIrq/Patched_SysErrIrq – Interrupt Handler Routine (triggered by
Interrupt)

FpuErrIrq/Patched_FpuErrIrq – Interrupt Handler Routine (triggered by
Interrupt)

AlgnErrIrq – Interrupt Handler Routine (triggered by Interrupt)

ResdOperIrq – Interrupt Handler Routine (triggered by Interrupt)

ExcpnHndlgInit1 – Non-RTE initialization function (called during startup
before RTE is initialized)

FeNmiPeg – Callout function for interrupt response handling (to be
called by FENMI Interrupt handler)

FeNmiSpiDblBit – Callout function for interrupt response handling (to be
called by FENMI Interrupt handler)

FeNmiDmaTrf – Callout function for interrupt response handling (to be
called by FENMI Interrupt handler)

FeNmiDmaRegAcsProtnErr – Callout function for interrupt response
handling (to be called by FENMI Interrupt handler)

FeNmiEcmMstChkrCmp – Callout function for interrupt response handling
(to be called by FENMI Interrupt handler)

FeNmiWdg – Callout function for interrupt response handling (to be
called by FENMI Interrupt handler)

FeNmiDtsDblBit – Callout function for interrupt response handling (to be
called by FENMI Interrupt handler)

ProcUkwnExcpnErr – Callout function for OS error response handling (to
be called by OS error handler)

ProcMpuExcpnErr – Callout function for OS error response handling (to be
called by OS error handler)

ProcPrvlgdInstrExcpnErr – Callout function for OS error response
handling (to be called by OS error handler)

ProcPrmntOsErr – Callout function for OS error response handling (to be
called by OS error handler)

ProcNonCritOsErr – Callout function for OS error response handling (to
be called by OS error handler)

# Configuration REQUIREMeNTS

## Build Time Config

|             |           |     |
|-------------|-----------|-----|
| **Modules** | **Notes** |     |
|             |           |     |

## Configuration Files to be provided by Integration Project

N/A

## Da Vinci Parameter Configuration Changes

|               |           |         |
|---------------|-----------|---------|
| **Parameter** | **Notes** | **SWC** |
|               |           |         |

## DaVinci Interrupt Configuration Changes

|                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------|-------------------------------------------|
| **ISR Name**          | **Notes**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Patched_SysErrIrq** | The ExcpnHndlg module implements an interrupt that needs a patch for a hardware problem that exists on the P1M hardware (see Renesas Technical Update TN-RH8-S001A/E). Nexteer has created the appropriate workaround that subsequently calls the normal interrupt handler code. Therefore, when configuring the SysErrIrq interrupt in the O/S the interrupt handler name should be configured to the Nexteer code with the workaround (“Patched_SysErrIrq”) instead of directly referencing the normal interrupt handler code. |
| **Patched_FpuErrIrq** | The ExcpnHndlg module implements an interrupt that needs a patch for a hardware problem that exists on the P1M hardware (see Renesas Technical Update TN-RH8-S001A/E). Nexteer has created the appropriate workaround that subsequently calls the normal interrupt handler code. Therefore, when configuring the FpuErrIrq interrupt in the O/S the interrupt handler name should be configured to the Nexteer code with the workaround (“Patched_FpuErrIrq”) instead of directly referencing the normal interrupt handler code. |

## Manual Configuration Changes

|              |           |         |
|--------------|-----------|---------|
| **Constant** | **Notes** | **SWC** |
|              |           |         |

# Integration DATAFLOW REQUIREMENTS

## Required Global Data Inputs

## Required Global Data Outputs

## Specific Include Path present

Yes

# Runnable Scheduling 

API usage and scheduling of BSW components expected to be captured at a
project architectural level and is beyond the scope of this document.
Third party documentation can be referenced as needed.

|                 |                                                             |                    |
|-------------------|---------------------------------------|---------------|
| **Init**        | **Scheduling Requirements**                                 | **Trigger**        |
| ExcpnHndlgInit1 | Pre-RTE initializaton                                       | Once at init       |
| ExcpnHndlgInit2 | After diagnostic manager is initialized and NTCs can be set | RTE initialization |
|                 |                                                             |                    |

|                    |                             |             |
|--------------------|-----------------------------|-------------|
| **Runnable**       | **Scheduling Requirements** | **Trigger** |
| **ExcpnHndlgPer1** |                             | 2ms         |

**.**

# Memory Map REQUIREMENTS

## Mapping

|                    |              |           |
|--------------------|--------------|-----------|
| **Memory Section** | **Contents** | **Notes** |
|                    |              |           |
|                    |              |           |

\* Each …START_SEC… constant is terminated by a …STOP_SEC… constant as
specified in the AUTOSAR Memory Mapping requirements.

## Usage

|             |         |         |
|-------------|---------|---------|
| **Feature** | **RAM** | **ROM** |
|             |         |         |

## NvM Blocks

# Compiler Settings

##  Preprocessor MACRO

## Optimization Settings

# Appendix

*\<This section is for appendix\>*

{% endraw %}