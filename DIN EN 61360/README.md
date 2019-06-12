The DIN EN 61360 [1] defines concepts to describe properties of technical systems. The properties are described as "data elements"
(e.g. lot size, filling level, error codes, live values, ...) and can be used to characterize a technical system.

Data elements can be described by a type description and an instance description. 
This brings the benefit of a uniform meta description that distinguishes between type descriptions, used to classify possible properties 
or characteristics in general, and instances that can be used to express certain values of a property (e.g. lot size = 4). 
The type description represents the characteristics of a physical or logical object that can be used to describe this object 
(e.g. unit of measure for the lot size). According to [1] the attributes of a type description can be classified as follows: 
-	Identifying attributes: e.g. ID, preferred name, version number
-	Semantic attributes: e.g. definition, source document for definition of the data element type, formula 
-	Value related attributes: e.g. data type, unit of measure, value list
-	Relational attributes: e.g. superordinate classes of the data element type
<br></br>
Please note, that all descriptions of attributes behind these four classes can be found in detail in [1].

Whenever a data element is instantiated, this data element receives an additional 
instance de-scription. The instance description complements the type description with further details, e.g. a measured value 
(e.g. lot size = “4”). In order to describe the data elements in a machine-interpretable way, attributes have to be used to further 
describe a type or an instance of a data element. 

With respect to [2], the attributes that represent the instance description of a data element are sub-sequently explained. 
The “Value” represents a measurable value of the instance. The attribute “Ex-pression Logic” can be used to indicate a 
logical interpretation of the value, e.g. less than/ greater than/ equal. The quality indicates the quality of the value, 
in means of quality of measure. The “Ex-pression Goal” is used to indicate whether a data element represents:
-	Requirements expression: the data element is used to describe a requirement (e.g. an order requires the lot size “4”)
-	Assurance expression: the data element is used to describe an assurance (e.g. a machine as-sures to produce with lot size “4”)
-	Present expression: the data element is used to describe a measured value (e.g. the actual produce lot size was “3”)

![](./pictures/DINEN61360_LWO.png?raw=true "DIN EN 61360 LWO")<br></br>
Figure 1: Type and instance description of data elements according to DIN EN 61360

Exemplary Competency Questions that could be answered with this ODP:<br></br>
Table 1: Example Competency Questions
![](./pictures/DINEN61360_exCQ.png?raw=true "exampleCQ")

[1]: DIN EN 61360-1. Standard data element types with associated classification scheme Part 1: Definitions - Principles and methods, 
06.2018 <br></br>
[2]: EPPLE, Ulrich: Merkmale als Grundlage der Interoperabilität technischer Systeme. 
In: at - Automa-tisierungstechnik 59 (2011), Nr. 7, S. 440–450 <br></br>
