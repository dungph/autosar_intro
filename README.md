# autosar_intro

My autosar learning journey

## Overview

Autosar architecture consist of 3 major part:

- SWC (Software component): the functional module (application software) drive the function of the ECU
- RTE (Runtime Environment): Middleware which connects the SWCs together or connect SWC to lower layer
- BSW (Base Software): Standardized software modules for the functioning of the higher layers

## Methodology

System Level development:

- System development defines Software Component, Hardware selection, Overall System and ECU Recourses.
    - Software Component and its Connection is defined
    - Software Component communicate over Virtual Functional Bus
    - VFB Enables SWCs independently be developed from other parts.

- Map Software Components to ECU based on Timing or Requirements. Generate System Configuration
- System Configuration includes BUS Mapping, Topology, etc. and mapping of SWC to ECU

ECU Development:

- ECU Extract: Extracts information from System Configuration description needed to the specific ECU.
- Output of ECU Ectract mainly contains `Flatview.arxml`, `Flatmap.arxml` and `EcuExtract.arxml`.
- Configure ECU: Additionally config the ECU: Task Scheduling, BSW config, Component Mapping, etc.
- Output of ECU configure is all inputs related to the mentioned ECU.
- Final RTE Layer: after have all information from the ECU, RTE Layer for that ECU will be generated for SWC develop.
