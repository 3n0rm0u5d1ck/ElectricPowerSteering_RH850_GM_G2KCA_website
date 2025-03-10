---
layout: default
title: MotQuadDetn_MDD
nav_order: 3
parent: Component Implementation
---
{% raw %}
**Module Design Document**

**For** **Motor Quadrant Detection**

**VERSION: 1.0**

**DATE: 11-MAY-2015**

**Prepared By:**

**Spandana Balani**

**Location:** The official version of this document is stored in the
Nexteer Configuration Management System.

**Revision History**

|             |                 |            |             |             |
|-------------|-----------------|------------|-------------|-------------|
| **Sl. No.** | **Description** | **Author** | **Version** | **Date**    |
| 1           | Initial Version | SB         | 1.0         | 11-May-2015 |
|             |                 |            |             |             |
|             |                 |            |             |             |
|             |                 |            |             |             |
|             |                 |            |             |             |

Table of Contents

[1 Abbrevations And Acronyms 5](#abbrevations-and-acronyms)

[2 References 6](#references)

[3 motquaddetn & High-Level Description
7](#motquaddetn-high-level-description)

[4 Design details of software module
8](#design-details-of-software-module)

[4.1 Graphical representation of MOtquaddetn
8](#graphical-representation-of-motquaddetn)

[4.2 Data Flow Diagram 8](#data-flow-diagram)

[4.2.1 Module level DFD 8](#module-level-dfd)

[4.2.2 Sub-Module level DFD 8](#sub-module-level-dfd)

[4.3 COMPONENT FLOW DIAGRAM 8](#component-flow-diagram)

[5 Variable Data Dictionary 9](#variable-data-dictionary)

[5.1 User defined typedef definition/declaration
9](#user-defined-typedef-definitiondeclaration)

[5.2 Variable definition for enumerated types
9](#variable-definition-for-enumerated-types)

[6 Constant Data Dictionary 10](#constant-data-dictionary)

[6.1 Program(fixed) Constants 10](#programfixed-constants)

[6.1.1 Embedded Constants 10](#embedded-constants)

[6.1.1.1 Local 10](#local)

[6.1.1.2 Global 10](#global)

[6.1.2 Module specific Lookup Tables Constants
10](#module-specific-lookup-tables-constants)

[7 Software Module Implementation 11](#software-module-implementation)

[7.1 Sub-Module Functions 11](#sub-module-functions)

[7.1.1 Initialization Functions 11](#initialization-functions)

[7.1.1.1 INIT: MotQuadDetnInit1 11](#init-motquaddetninit1)

[7.1.1.2 Design Rationale 11](#design-rationale)

[7.1.1.3 Store Module Inputs to Local copies
11](#store-module-inputs-to-local-copies)

[7.1.1.4 (Processing of function)……… 11](#processing-of-function)

[7.1.1.5 Store Local copy of outputs into Module Outputs
11](#store-local-copy-of-outputs-into-module-outputs)

[7.1.2 PERIODIC FUNCTIONS 11](#periodic-functions)

[7.1.2.1 Per: MotQuadDetnPer1 11](#per-motquaddetnper1)

[7.1.2.2 Design Rationale 11](#design-rationale-1)

[7.1.2.3 Store Module Inputs to Local copies
11](#store-module-inputs-to-local-copies-1)

[7.1.2.4 (Processing of function)……… 11](#processing-of-function-1)

[7.1.2.5 Store Local copy of outputs into Module Outputs
11](#store-local-copy-of-outputs-into-module-outputs-1)

[7.2 Interrupt Functions 11](#interrupt-functions)

[7.3 Serial Communication Functions 12](#serial-communication-functions)

[7.4 Local Function/Macro Definitions
12](#local-functionmacro-definitions)

[7.5 GLObAL Function/Macro Definitions
12](#global-functionmacro-definitions)

[7.6 TRANSIENT FUNCTIONS 12](#transient-functions)

[8 Known Limitations With Design 13](#known-limitations-with-design)

[9 UNIT TEST CONSIDERATION 14](#unit-test-consideration)

[10 Appendix 15](#appendix)

# Abbrevations And Acronyms

|              |                                         |
|--------------|-----------------------------------------|
| Abbreviation | Description                             |
| DFD          | Design functional diagram               |
| MDD          | Module design Document                  |
|              | \<ADD more to the table if applicable\> |
|              |                                         |

# References

This section lists the title & version of all the documents that are
referred for development of this document

|         |                                       |                                |
|----------|----------------------------------------------|-----------------|
| Sr. No. | Title                                 | Version                        |
| \<1\>   | \<MDD Guidelines\>                    | Process 3.06.00                |
| \<2\>   | \<Software Naming Conventions\>       | Process 3.06.00                |
| \<3\>   | \<Coding standards\>                  | Process 3.06.00                |
| \<4\>   | FDD – SF101A Motor Quadrant Detection | See Synergy Subproject version |
|         | \<Add if more available\>             |                                |

# motquaddetn & High-Level Description

*None*

# Design details of software module

## Graphical representation of MOtquaddetn

<img
src="ElectricPowerSteering_RH850_GM_G2KCA_website/docs/SF101A_MotQuadDetn_Impl/doc/mediax/media/image1.png"
style="width:2.41667in;height:2.72917in" />

## Data Flow Diagram

## Module level DFD

*N/A*

## Sub-Module level DFD

*N/A*

## COMPONENT FLOW DIAGRAM

*N/A*

# Variable Data Dictionary

## User defined typedef definition/declaration 

*\<This section documents any user types uniquely used for the
module.\>*

<table>
<colgroup>
<col style="width: 34%" />
<col style="width: 31%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Typedef Name</td>
<td>Element Name</td>
<td>User Defined Type</td>
<td><p>Legal Range</p>
<p>(min)</p></td>
<td><p>Legal Range</p>
<p>(max)</p></td>
</tr>
<tr class="even">
<td>N/A</td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## Variable definition for enumerated types

|           |              |       |
|-----------|--------------|-------|
| Enum Name | Element Name | Value |
| N/A       |              |       |

# Constant Data Dictionary

## Program(fixed) Constants

## Embedded Constants

*\< All program specific constants will be defined in detail \>*

## Local

|                              |            |       |       |
|------------------------------|------------|-------|-------|
| Constant Name                | Resolution | Units | Value |
| Refer constants from .m file |            |       |       |

## Global

*\<This section lists the global constants used by the module. For
details on global constants, refer to the Data Dictionary for the
application\>*

|               |
|---------------|
| Constant Name |
| N/A           |
|               |
|               |

## Module specific Lookup Tables Constants

*\<(This is for lookup tables (arrays) with fixed values, same name as
other tables)\>*

|                                            |                                |                                |                                |
|------------------------------|----------------|--------------|--------------|
| Constant Name                              | Resolution                     | Value                          | Software Segment               |
| \<Refer Constant name qualified in \[2\]\> | \<Refer MDD guidelines \[1\]\> | \<Refer MDD guidelines \[1\]\> | \<Refer MDD guidelines \[1\]\> |

# Software Module Implementation

## Sub-Module Functions

None

## Initialization Functions

## INIT: MotQuadDetnInit1

## Design Rationale

*None*

## Store Module Inputs to Local copies

*Refer to FDD*

## (Processing of function)………

*Refer to FDD*

## Store Local copy of outputs into Module Outputs

*Refer to FDD*

## PERIODIC FUNCTIONS 

*(Note: For multiple periodic functions, insert new headers at the
“Header 2” level – subset of “7.1.2 Periodic Functions” and follow the
same sub-section design shown below). If none required, place the text
“None”)\>*

## Per: MotQuadDetnPer1

## Design Rationale

## Store Module Inputs to Local copies

*Refer to FDD*

## (Processing of function)………

*Refer to FDD*

## Store Local copy of outputs into Module Outputs

*Refer to FDD*

## Interrupt Functions

*None*

## Serial Communication Functions

*None*

## Local Function/Macro Definitions

None

## GLObAL Function/Macro Definitions

None

## TRANSIENT FUNCTIONS 

*None*

# Known Limitations With Design

Rollover Checking is not needed. Fixed point math implementation takes
care of it and no additional logic is required.

# UNIT TEST CONSIDERATION

*None*

# Appendix

*None*

{% endraw %}