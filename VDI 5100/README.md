The VDI 5100 [1] describes a system architecture for intralogistics. SAIL is an architectural model used to describe components for Intralogistic systems as well as their basic functions and principle interfaces.

The SAIL model is a result of a paradigm shift inspired by object-oriented programming. Within this context, the top-down sub-division is undertaken according to the functional organisation of the facility. 

Entities withing the SAIL model can be categorized in x categories, each with their own subclassification. These are Functions (F), Components (C) and Information Interfaces (I).

Functions:
- FacilityControl             – F:FC
- InformationCollection       – F:IC
- DirectionControl            – F:DC
- MissionManagement           – F:MM
- ResourceUtilisation         – F:RU
- TransportCoordination       – TC

Components:
Basic Components:
- ConveyingElement            – C:CE
- InformationElement          – C:IE

Aggregation Components:
- ConveyingGroup              – C:CG
- ConveyingSegment            – C:CS
- ConveyingArea               – C:CA

Information Interfaces:
- TransportOrder              - I:TO
- TransportOrderCancellation  - I:TOC
- TransportOrderDone          - I:TOD
- Mission                     - I:M
- MissionCancellation         - I:MC
- MissionRequest              - I:MR
- OperatingParameter          - I:OP
- Notification                - I:NO
- FacilityStatus              - I:FS
- DirectionInformation        - I:DI
- DirectionRequest            - I:DR
- SensorInformation           - I:SI

Additional information on which kinds of components can communicate via which kind of information interfaces as well as information on functions performed by components can be found in [1].


[1]: VDI/VDMA 5100. System architecture for intralogistics (SAIL) Part 1: Fundamentals, 
05.2016 <br></br>
