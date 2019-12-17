# Web Application Description Language (WADL)
## Introduction
The Web Application Description Language defines modelling elements that can be used to formally describe (RESTful) Webservices and how to interact with them. It has been proposed for standardization as a so called "W3C Member Submission". The official W3C document can be found under https://www.w3.org/Submission/wadl/#x3-150002.8. The original W3C Member Submission defined an XML-Schema to describe Webservices. We took this Schema and converted it into a TBox of OWL ontology.
## Important concepts
The following list provides an overview of the most important concepts of the WADL ontology design pattern:
- **Resources**: A  *Resources* element defines the root element of a webservice. It can be seen as the webserver that provides access to a variety of different resources. One important aspect of a *Resources* element is that it carries the base path of all the *Resource* elements that are connected to it.  
- **Resource**: A *Resource* element can be used to describe one resource that can be accessed on a given webserver. A resource can be a document (e.g. HTML) or other kind of data. Every resource has a path that is used together with the base path of the parent *Resource* element to identify the resource. 
Disclaimer: We apologize for the poor and confusing naming of *Resources* and *Resource*. But we didn't come up with this naming, it has been directly taken from the WADL standard.
- **Method**: *Methods* are used to model different HTTP-Methods that can be used on a *Resource*. While request using the GET-Method are typically used to retrieve a resource, POST and PUT methods are used to add a resource or change an existing one, respectively. This ODP currently supports the most commonly used HTTP methods GET, POST. PUT, PATCH, DELETE.
- **Request**: To be able to successfully interact with a resource, a user (human or machine) has to know what information has to be sent with a request against a resource. Such request information typically include media type and (a set of) parameters
- **Response**: After sending a request, a client waits for the response of the webserver. The format and parameters of possible reponses can be modelled with *Response* elements.
- **Representation**: A *Representation* stands for one possible media type. It can be used for both modelling of request and responses.
- **Parameter**: *Parameters* can also be used to model requests and responses. When modelling requests, parameters are used to describe which information is necessary in order to interact with a webserver. When used with responses, parameters are used to model the structure of possible responses
## Example
The following subsections show examples that hopefully help in better understanding our ODP for the Web Application Description Language and to give exemplary SPARQL updates and queries.
### Graphical example
The following image shows an exemplary webservice that allows to add users to a collection. All resources of the server can be found under the base path "mydomain.com/resources". The example contains only one resource, the one to add users. This resource has the path "/users", so it can be reached under "mydomain.com/resources/users". While in reality, there might be multiple methods to retrieve one / all users and to edit information of existing users, this example shows only one method, an HTTP POST. The upper section of the graph consists of all elements neccessary for a request. Because the example shows a POST request, it is important to describe the media type of the information that have to be supplied in the request body. In this case, the media type is specified as "application/json". Two parameters are required: name and EMail-Adress of the user that is going to be added.
The lower section shows how to model a response. The representation of the response (body) has the same media type as the request ("application/json") and it contains only one parameter, which is an information about whether or not the request was executed successfully.

![Example of request and response of a single resource provided by a webserver](https://github.com/ConstantinHildebrandt/Industrial-Standard-Ontology-Design-Patterns/blob/images/wadl/WADL/WADL-Example.png)

Please note that this example shows most but not all of the concepts. Please refer to rdfs:comments of the ODP itself for properties not shown in this example. 
### SPARQL Update
...coming soon

### SPARQL Query
... coming soon