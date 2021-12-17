:warning: This repo has been archived. All ODPs are now maintained in separate repositories to better keep track of the versions. :warning: <br>
You can find these separate repositories here:
 - [DIN EN 61360](https://github.com/hsu-aut/IndustrialStandard-ODP-DINEN61360)
 - [VDI 2206](https://github.com/hsu-aut/IndustrialStandard-ODP-VDI2206)
 - [VDI 2860](https://github.com/hsu-aut/IndustrialStandard-ODP-VDI2860)
 - [VDI 3682](https://github.com/hsu-aut/IndustrialStandard-ODP-VDI3682)
 - [DIN 8580](https://github.com/hsu-aut/IndustrialStandard-ODP-DIN8580)
 - [ISA 88](https://github.com/hsu-aut/IndustrialStandard-ODP-ISA88)
 - [WADL](https://github.com/hsu-aut/IndustrialStandard-ODP-WADL)
 - [DIN EN 62264-2](https://github.com/hsu-aut/IndustrialStandard-ODP-DINEN62264-2)
 - [OPC UA](https://github.com/hsu-aut/IndustrialStandard-ODP-OPC-UA)
 - [ISO 22400-2](https://github.com/hsu-aut/IndustrialStandard-ODP-ISO22400-2)

# Industrial-Standard-Ontology-Design-Patterns

The development of software functionalities, or applications in general, that monitor and analyze manufacturing related data in order to improve, support or automate processes, is becoming increasingly important in industry. These applications require several information from different data sources in their context. An application that is planning a maintenance workers daily schedule for instance, requires several information about machine statuses, production plans and inventory, which resides in different systems likes Programmable Logical Controllers (PLC) or Structured Query Language (SQL) databases. Furthermore, manufacturing companies usually run machines and software systems from different vendors or of different ages. The schemata used in such systems do therefor not follow a certain standard, i.e. they are very heterogeneous in their semantics. When building such applications, accessing, searching and understanding the data sources is becoming a very time intensive, manual and error prone procedure that is repeated for every newly build application and for every newly introduced data source. To allow for an eased access, searching and understanding of these heterogeneous data sources, an ontology can be used to integrate all heterogeneous data sources in one schemata. 

The ontologies within this repository are based on industrial standards (e.g. ISO, DIN EN, VDI/VDE etc.), hence, the ontologies use the vocabulary and technical concept of these standards, i.e. the ontologies formalize the knowledge contained in these standards.

## Usage
If you want to use any of these ontology design patterns, the easiest way is to directly import them into your ontology via `owl:imports` statements. Make sure to reference a fixed release version so that you can't get surprised by future changes. To do so, click on the branch selection right below the number of commits and select a tag from the dropdown, e.g. v1.2.0. Then navigate to the .owl-file of the ODP you want to use, lets say VDI3682.owl. Open the raw file of this file. For this example it would be https://raw.githubusercontent.com/hsu-aut/Industrial-Standard-Ontology-Design-Patterns/v1.2.0/VDI%203682/VDI3682.owl. You can use this URL in an `owl:imports` statement of your ontology. If you're having trouble using this URL in a tool like Protégé, try opening your ontology with a text editor and simply inserting your imports manually.
An example of an imports section with a couple of ODPs looks like this:

```xml
<owl:Ontology rdf:about="http://www.hsu-ifa.de/ontologies/capability-model#">
    <owl:versionIRI rdf:resource="http://www.hsu-ifa.de/ontologies/capability-model/1.0.0#"/>
    <owl:imports rdf:resource="https://raw.githubusercontent.com/hsu-aut/Industrial-Standard-Ontology-Design-Patterns/v1.2.0/DIN%208580/DIN8580.owl"/>
    <owl:imports rdf:resource="https://raw.githubusercontent.com/hsu-aut/Industrial-Standard-Ontology-Design-Patterns/v1.2.0/DIN%20EN%2061360/DINEN61360.owl"/>
    <owl:imports rdf:resource="https://raw.githubusercontent.com/hsu-aut/Industrial-Standard-Ontology-Design-Patterns/v1.2.0/OPC%20UA/OpcUa.owl"/>
    <owl:imports rdf:resource="https://raw.githubusercontent.com/hsu-aut/Industrial-Standard-Ontology-Design-Patterns/v1.2.0/VDI%202206/VDI2206.owl"/>
    <owl:imports rdf:resource="https://raw.githubusercontent.com/hsu-aut/Industrial-Standard-Ontology-Design-Patterns/v1.2.0/VDI%202860/VDI2860.owl"/>
    <owl:imports rdf:resource="https://raw.githubusercontent.com/hsu-aut/Industrial-Standard-Ontology-Design-Patterns/v1.2.0/VDI%203682/VDI3682.owl"/>
    <owl:imports rdf:resource="https://raw.githubusercontent.com/hsu-aut/Industrial-Standard-Ontology-Design-Patterns/v1.2.0/WADL/WADL.owl"/>
</owl:Ontology>
```
Of course you can also clone or download this repository and import an ODP from a local copy. The advantage of the first approach is that tools like Protégé or TopBraid Composer will directly use the ontologies from the internet and you can simply increase the version number in case you want to use a newer version of our ODPs.

## Tool Support
In case you want to make creating individuals from these TBoxes a lot easier, check out our 'Lightweight Industrial Ontology Design Support Tool' (LiOnS). It is designed to create RDF models using the Ontology Design Patterns of this repository. This enables users to:
- Semi-automatically design RDF models (only variable parts of the graph have to be defined)
- Consistent modelling, without being an ontology expert
- Downloading Turtle serialized models or SPARQL INSERTs

For more information, see https://github.com/ConstantinHildebrandt/lion.

## Further reading:
- C. Hildebrandt, A. Scholz, A. Fay, T. Schröder, T. Hadlich, C. Diedrich, M. Dubovy, C. Eck, R. Wiegand: Semantic Modeling for Collaboration and Cooperation of Systems in the production domain. In: 22nd IEEE Emerging Technology and Factory Automation (ETFA), 2017.
-  C. Hildebrandt, S. Törsleff, T. Bandyszak, B. Caesar, A. Ludewig, A. Fay: Ontology Engineering for Collaborative Embedded Systems – Requirements and Initial Approach. In: Schäfer, Karagiannis (Hrsg.): Fachtagung Modellierung, 2018.
- C. Hildebrandt, S. Törsleff, B. Caesar, A. Fay: Ontology Building for Cyber-Physical Systems: A domain expert centric approach. In: 2018 14th IEEE Conference on Automation Science and Engineering (CASE 2018), 2018.
