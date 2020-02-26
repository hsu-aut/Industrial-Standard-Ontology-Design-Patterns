The ISO 22400-2 presents KPIs for Manufacturing Operations Management (MOM) by terminologically standardizing various KPI-related terms, 
but also providing formulas for their calculation. In addition, the ISO 22400-2 references the asset hierarchy defined in 
DIN EN 62264-2. By referring to the asset hierarchy of DIN EN 62264-2, all competency questions that are aiming at structural correlations 
should be able to be answered using ISO 22400-2 as well. 

In this way, ISO 22400-2 also acts as a standardized matcher of KPI descriptions with structure descriptions. The Lightweight Ontology of 
the ISO 22400-2 can be found in the subsequent Figure 1. There are mainly three categories of KPIs, which are Production, Maintenance, 
Inventory and Quality. Each category holds a set of KPIs. Each KPI has a set of DataTypeProperties (Attributes) that can describe the KPI. 
Furthermore, there are a couple of annotations specific to every KPI and parameter. Every KPI may contain complex arguments in the 
sense that a KPI is calculated based on another KPI. Some KPIs may only have simple arguments in the sense of parameters like 
"Actual Production Time". Parameters also have annotaions specific to them and a set of attributes.

![](./pictures/ISO22400-2.png?raw=true "ISO 22400-2 LWO")<br></br>
Figure 1: Key Performance Indicators according to ISO 22400-2

Exemplary competency questions that may be anwered by using this Ontology-Design Pattern can be found in Table 1. SPARQL patterns that
create KPIs or their parameters can be found in the sub-folders of this directory.

Table 1: Exemplary competency questions and answers specific to ISO 22400-2
![](./pictures/ISO22400-2_exCQ.png?raw=true "ISO 22400-2 CQ")<br></br>
