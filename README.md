Markdown documentation created by [pyLODE](http://github.com/rdflib/pyLODE) 2.4

# Level of Information Need (LOIN) Ontology

## Metadata
* **IRI**
  * `http://www.inf.bi.rub.de/loin/ns`
* **Publisher(s)**
  * [Chair of Computing in Engineering, Ruhr University Bochum](https://www.inf.bi.rub.de)
* **Creators(s)**
  * [Liu Liu](https://orcid.org/0000-0001-5907-7609)
    [[ORCID]](https://orcid.org/0000-0001-5907-7609)
    (<liu.liu-m6r@rub.de></a>) of [Ruhr University Bochum](https://www.inf.bi.ruhr-uni-bochum.de/iib/lehrstuhl/mitarbeiter/liu_liu.html.en)
  * [Philipp Hagedorn](https://orcid.org/0000-0002-6249-243X)
    [[ORCID]](https://orcid.org/0000-0002-6249-243X)
    (<philipp.hagedorn-n6v@rub.de></a>) of [Ruhr University Bochum](https://www.inf.bi.ruhr-uni-bochum.de/iib/lehrstuhl/mitarbeiter/philipp_hagedorn.html.en)
* **Created**
  * 2023-01-30
* **Version Information**
  * 0.1
* **Imports**
  * [https://standards.iso.org/iso/21597/-1/ed-1/en/Container](https://standards.iso.org/iso/21597/-1/ed-1/en/Container)
  * [https://standards.iso.org/iso/21597/-1/ed-1/en/Linkset](https://standards.iso.org/iso/21597/-1/ed-1/en/Linkset)
* **License &amp; Rights**
  * [https://creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/)
  * &copy; 2023 by Chair of Computing in Engineering, Ruhr University Bochum
* **Source**
  * [https://github.com/RUB-Informatik-im-Bauwesen/loin-ontology](https://github.com/RUB-Informatik-im-Bauwesen/loin-ontology)
* **Ontology RDF**
  * RDF ([loin.ttl](turtle))
### Description
<p>The Level of Information Need (LOIN) Ontology is defined for specifying information requirements for delivery of data in a buildings' life cycle. The LOIN ontology is based on the standard BS EN 17412-1 (2020). Furthermore, it is extended with vocabulary for connecing Information Delivery Specifications (IDS) and Information containers for linked document delivery (ICDD) as per ISO 21597-1 (2020). </p>

## Table of Contents
1. [Classes](#classes)
1. [Object Properties](#objectproperties)
1. [Datatype Properties](#datatypeproperties)
1. [Annotation Properties](#annotationproperties)
1. [Properties](#properties)
1. [Namespaces](#namespaces)
1. [Legend](#legend)


## Overview

**Figure 1:** Ontology overview
## Classes
[Actor](#Actor),
[Alphanumerical information](#Alphanumericalinformation),
[Alphanumerical information content](#Alphanumericalinformationcontent),
[Appearance](#Appearance),
[Attribut](#Attribut),
[Attribute name](#Attributename),
[Breakdown structure](#Breakdownstructure),
[Breakdown structure type](#Breakdownstructuretype),
[Classification](#Classification),
[Detail](#Detail),
[Dimensionality](#Dimensionality),
[Document](#Document),
[Document content](#Documentcontent),
[Document format](#Documentformat),
[Document purpose](#Documentpurpose),
[Document specification](#Documentspecification),
[Documentation](#Documentation),
[Entity](#Entity),
[Entity name](#Entityname),
[Geometrical information](#Geometricalinformation),
[Geometrical information specification](#Geometricalinformationspecification),
[IDS data definition](#IDSdatadefinition),
[IDS facet Definition](#IDSfacetDefinition),
[IDS facet parameter](#IDSfacetparameter),
[IDS requirement type](#IDSrequirementtype),
[IFC data type](#IFCdatatype),
[Identification](#Identification),
[Identifier](#Identifier),
[Identifier type](#Identifiertype),
[Information delivery milestone](#Informationdeliverymilestone),
[Information provider](#Informationprovider),
[Information receiver](#Informationreceiver),
[Location](#Location),
[Material](#Material),
[Object](#Object),
[Ontology data definition](#Ontologydatadefinition),
[Parametric behaviour](#Parametricbehaviour),
[Predefined type](#Predefinedtype),
[Property](#Property),
[Property name](#Propertyname),
[Property set name](#Propertysetname),
[Purpose](#Purpose),
[Restriction type](#Restrictiontype),
[Value](#Value),
### Actor
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#Actor`
Description | <p>Actor is a contextual aspect according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Sub-classes |[loin:InformationProvider](Informationprovider) (c)<br />[loin:InformationReceiver](Informationreceiver) (c)<br />
In domain of |[loin:hasAgent](hasagent) (op)<br />[loin:isRelatedToContainerParty](isrelatedtocontainerparty)<br />
### Appearance
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#Appearance`
Description | <p>Appearance as a geometrical information specification for information need according to BS EN 17412-1 (2020)</p>
Super-classes |[loin:GeometrySpecification](Geometricalinformationspecification) (c)<br />
In range of |[loin:hasAppearance](hasappearance) (op)<br />
### Attribut
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#Attribute`
Description | <p>Attribut is an IDS facet according to IDS developed by buildingSMART International</p>
Super-classes |[loin:IDSFacetDefinition](IDSfacetDefinition) (c)<br />
Restrictions |[loin:hasAttributeName](hasattributename) (op) **exactly** 1<br />
In domain of |[loin:hasAttributeName](hasattributename) (op)<br />[loin:hasValue](hasvalue) (op)<br />
### Attribute name
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#AttributeName`
Description | <p>Attribute name must be a valid attribute name from the IFC schema according to IDS developed by buildingSMART International. Example AttributeName = "Description"</p>
Super-classes |[loin:IDSFacetParameter](IDSfacetparameter) (c)<br />
Restrictions |[loin:RestrictionFormulation](RestrictionFormulation) (dp) **exactly** 1<br />[loin:hasRestrictionType](hasrestrictiontype) (op) **value** [loin:SimpleValue](http://www.inf.bi.rub.de/loin/ns#SimpleValue) (c)<br />
In range of |[loin:hasAttributeName](hasattributename) (op)<br />
### Breakdown structure
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#BreakdownStructure`
Description | <p>Breakdown structure is a term for positioning the object in a structure according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Restrictions |[loin:hasIdentifier](hasidentifier) (op) **exactly** 1<br />
In domain of |[loin:hasIdentifier](hasidentifier) (op)<br />[loin:hasBreakdownStructureType](hasbreakdownstructuretype) (op)<br />
In range of |[loin:hasBreakdownStructure](hasbreakdownstructure) (op)<br />
### Breakdown structure type
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#BreakdownStructureType`
Description | <p>Breakdown structure type is a term to specify the structure according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
In range of |[loin:hasBreakdownStructureType](hasbreakdownstructuretype) (op)<br />
### Classification
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#Classification`
Description | <p>Classification is an IDS facet according to IDS developed by buildingSMART International</p>
Super-classes |[loin:IDSFacetDefinition](IDSfacetDefinition) (c)<br />
### Detail
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#Detail`
Description | <p>Detail as a geometrical information specification for information need according to BS EN 17412-1 (2020)</p>
Super-classes |[loin:GeometrySpecification](Geometricalinformationspecification) (c)<br />
In range of |[loin:hasDetail](hasdetail) (op)<br />
### Dimensionality
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#Dimensionality`
Description | <p>Dimensionality as a geometrical information specification for information need according to BS EN 17412-1 (2020)</p>
Super-classes |[loin:GeometrySpecification](Geometricalinformationspecification) (c)<br />
In range of |[loin:hasDimensionality](hasdimensionality) (op)<br />
### Document
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#Document`
Description | <p>Document is a term for specifying the documentation of information need according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Restrictions |[loin:hasDocumentSpecification](hasdocumentatonspecification) (op) **some** [loin:DocumentFormat](Documentformat) (c)<br />[loin:belongsToInformationContent](belongstoinformationcontent) (op) **max** 1<br />[loin:hasDocumentSpecification](hasdocumentatonspecification) (op) **some** [loin:DocumentPurpose](Documentpurpose) (c)<br />[loin:isRelatedToContainerDocument](isrelatedtocontainerdocument) (op) **max** 1<br />[loin:hasDocumentSpecification](hasdocumentatonspecification) (op) **some** [loin:DocumentContent](Documentcontent) (c)<br />[loin:isRelatedToContainerLinkset](isrelatedtocontainerlinkset) (op) **max** 1<br />
In domain of |[loin:belongsToInformationContent](belongstoinformationcontent) (op)<br />[loin:isRelatedToContainerLinkset](isrelatedtocontainerlinkset) (op)<br />[loin:isRelatedToContainerDocument](isrelatedtocontainerdocument) (op)<br />[loin:hasDocumentSpecification](hasdocumentatonspecification) (op)<br />
In range of |[loin:isRelatedToLoinDocument](isrelatedtoLoindocument) (op)<br />
### Document content
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#DocumentContent`
Description | <p>Document specification for content for information need according to BS EN 17412-1 (2020)</p>
Super-classes |[loin:DocumentSpecification](Documentspecification) (c)<br />
### Document format
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#DocumentFormat`
Description | <p>Document specification for format for information need according to BS EN 17412-1 (2020)</p>
Super-classes |[loin:DocumentSpecification](Documentspecification) (c)<br />
### Document purpose
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#DocumentPurpose`
Description | <p>Document specification for purpose for information need according to BS EN 17412-1 (2020)</p>
Super-classes |[loin:DocumentSpecification](Documentspecification) (c)<br />
### Document specification
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#DocumentSpecification`
Description | <p>Additional specification of document for information need according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Sub-classes |[loin:DocumentFormat](Documentformat) (c)<br />[loin:DocumentPurpose](Documentpurpose) (c)<br />[loin:DocumentContent](Documentcontent) (c)<br />
In range of |[loin:hasDocumentSpecification](hasdocumentatonspecification) (op)<br />
### Documentation
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#Documentation`
Description | <p>Documentation is a term for specifying the information need according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
In domain of |[loin:hasDocument](hasdocument) (op)<br />
In range of |[loin:hasDocumentation](hasdocumentation) (op)<br />
### Entity
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#Entity`
Description | <p>Entity is an IDS facet according to IDS developed by buildingSMART International</p>
Super-classes |[loin:IDSFacetDefinition](IDSfacetDefinition) (c)<br />
Restrictions |[loin:hasEntityName](hasentityname) (op) **exactly** 1<br />
In domain of |[loin:hasEntityName](hasentityname) (op)<br />[loin:hasPredefinedType](haspredefinedtype) (op)<br />
### Entity name
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#EntityName`
Description | <p>Entity name must be a valid IFC class from the IFC schema according to IDS developed by buildingSMART International. Example EntityName = "IFCWALL"</p>
Super-classes |[loin:IDSFacetParameter](IDSfacetparameter) (c)<br />
Restrictions |[loin:hasRestrictionType](hasrestrictiontype) (op) **exactly** 1<br />
In range of |[loin:hasEntityName](hasentityname) (op)<br />
### Geometrical information
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#Geometry`
Description | <p>Geometrical information is a term for specifying the information need according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Restrictions |[loin:hasGeometrySpecification](hasgeometricalinformationspecification) (op) **some** [loin:Appearance](Appearance) (c)<br />[loin:hasGeometrySpecification](hasgeometricalinformationspecification) (op) **some** [loin:Location](Location) (c)<br />[loin:requested](requested) (dp) **exactly** 1<br />[loin:hasGeometrySpecification](hasgeometricalinformationspecification) (op) **some** [loin:ParametricBehaviour](Parametricbehaviour) (c)<br />[loin:hasGeometrySpecification](hasgeometricalinformationspecification) (op) **some** [loin:Detail](Detail) (c)<br />[loin:hasGeometrySpecification](hasgeometricalinformationspecification) (op) **some** [loin:Dimensionality](Dimensionality) (c)<br />
In domain of |[loin:requested](requested) (dp)<br />[loin:hasGeometrySpecification](hasgeometricalinformationspecification) (op)<br />
In range of |[loin:hasGeometry](hasgeometricalinformation) (op)<br />
### Geometrical information specification
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#GeometrySpecification`
Description | <p>Additional specification of geometrical information for information need according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Sub-classes |[loin:Location](Location) (c)<br />[loin:Appearance](Appearance) (c)<br />[loin:Detail](Detail) (c)<br />[loin:Dimensionality](Dimensionality) (c)<br />[loin:ParametricBehaviour](Parametricbehaviour) (c)<br />
In domain of |[loin:requested](requested) (dp)<br />
In range of |[loin:hasGeometrySpecification](hasgeometricalinformationspecification) (op)<br />
### IDS data definition
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#IDSDataDefinition`
Description | <p>IDS data definition is used to specify the alphanumerical information according to IDS developed by buildingSMART International</p>
Super-classes |[loin:InformationContent](Alphanumericalinformationcontent) (c)<br />
Restrictions |[loin:description](description) (dp) **exactly** 1<br />[loin:hasApplicability](hasapplicability) (op) **min** 1<br />[loin:hasRequirement](hasrequirement) (op) **min** 1<br />[loin:hasApplicability](hasapplicability) (op) **some** [loin:Entity](Entity) (c)<br />[loin:specifiedByIdentifier](specifiedbyidentifier) **max** 0<br />
In domain of |[loin:hasApplicability](hasapplicability) (op)<br />[loin:hasRequirement](hasrequirement) (op)<br />
### IDS facet Definition
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#IDSFacetDefinition`
Description | <p>IDS facet definition is used to define a facet to apply the requirement or to require the information according to IDS developed by buildingSMART International</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Sub-classes |[loin:Property](Property) (c)<br />[loin:Material](Material) (c)<br />[loin:Entity](Entity) (c)<br />[loin:Attribute](Attribut) (c)<br />[loin:Classification](Classification) (c)<br />
In domain of |[loin:hasRequirementType](hasrequirementtype) (op)<br />
In range of |[loin:hasRequirement](hasrequirement) (op)<br />[loin:hasApplicability](hasapplicability) (op)<br />
### IDS facet parameter
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#IDSFacetParameter`
Description | <p>IDS facet parameter is used to specify a facet definition according to IDS developed by buildingSMART International</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Sub-classes |[loin:IFCDataType](IFCdatatype) (c)<br />[loin:AttributeName](Attributename) (c)<br />[loin:Value](Value) (c)<br />[loin:PredefinedType](Predefinedtype) (c)<br />[loin:PropertyName](Propertyname) (c)<br />[loin:EntityName](Entityname) (c)<br />[loin:PsetName](Propertysetname) (c)<br />
In domain of |[loin:RestrictionFormulation](RestrictionFormulation) (dp)<br />[loin:hasRestrictionType](hasrestrictiontype) (op)<br />
### IDS requirement type
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#IDSRequirementType`
Description | <p>IDS requirement type is used to specify a requirement, if it is optional or mandatory according to IDS developed by buildingSMART International</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
In range of |[loin:hasRequirementType](hasrequirementtype) (op)<br />
### Restriction type
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#IDSRestrictionType`
Description | <p>Restriction type is used to define the value of IDS facet parameter according to IDS developed by buildingSMART International</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
In range of |[loin:hasRestrictionType](hasrestrictiontype) (op)<br />
### IFC data type
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#IFCDataType`
Description | <p>IFC data type must be a valid predefined type from the IFC schema according to IDS developed by buildingSMART International</p>
Super-classes |[loin:IDSFacetParameter](IDSfacetparameter) (c)<br />
Restrictions |[loin:hasRestrictionType](hasrestrictiontype) (op) **value** [loin:SimpleValue](http://www.inf.bi.rub.de/loin/ns#SimpleValue) (c)<br />[loin:RestrictionFormulation](RestrictionFormulation) (dp) **exactly** 1<br />
In range of |[loin:hasIFCDataType](hasIFCdatatype) (op)<br />
### Identification
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#Identification`
Description | <p>Identification is a term for positioning the object in a breakdown structure according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Restrictions |[loin:hasBreakdownStructure](hasbreakdownstructure) (op) **min** 1<br />
In domain of |[loin:hasBreakdownStructure](hasbreakdownstructure) (op)<br />
In range of |[loin:hasIdentification](hasidentification) (op)<br />
### Identifier
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#Identifier`
Description | <p>Identifier is used to assiging a vaule for positioning the object in a breakdown structure according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Restrictions |[loin:value](value) (dp) **exactly** 1<br />[loin:hasBreakdownStructure](hasbreakdownstructure) (op) **exactly** 1<br />[loin:hasIdentifierType](hasidentifiertype) (op) **exactly** 1<br />
In domain of |[loin:hasIdentifierType](hasidentifiertype) (op)<br />
In range of |[loin:hasIdentifier](hasidentifier) (op)<br />[loin:specifiedByIdentifier](specifiedbyidentifier)<br />
### Identifier type
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#IdentifierType`
Description | <p>Identifier type is used to specify the identifier in a breakdown structure according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
In domain of |[loin:isRelatedToLinksetIdentifier](isrelatedtolinksetidentifier)<br />
In range of |[loin:hasIdentifierType](hasidentifiertype) (op)<br />
### Alphanumerical information
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#Information`
Description | <p>Alphanumerical information is a term for specifying the information need according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Restrictions |[loin:requested](requested) (dp) **exactly** 1<br />
In domain of |[loin:hasInformationContent](hasalphanumericalinformatoncontent) (op)<br />[loin:requested](requested) (dp)<br />[loin:hasIdentification](hasidentification) (op)<br />
In range of |[loin:hasInformation](hasalphanumericalinformation) (op)<br />
### Alphanumerical information content
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#InformationContent`
Description | <p>Alphanumerical information content is a term for specifying the alphanumerical information according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Sub-classes |[loin:OntologyDataDefinition](Ontologydatadefinition) (c)<br />[loin:IDSDataDefinition](IDSdatadefinition) (c)<br />
In domain of |[loin:isRelatedToLoinDocument](isrelatedtoLoindocument) (op)<br />[loin:specifiedByIdentifier](specifiedbyidentifier)<br />
In range of |[loin:hasInformationContent](hasalphanumericalinformatoncontent) (op)<br />[loin:belongsToInformationContent](belongstoinformationcontent) (op)<br />
### Information delivery milestone
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#InformationDeliveryMilestone`
Description | <p>Information delivery milestone is a contextual aspect according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Restrictions |[loin:hasReceiver](hasinformationreceiver) (op) **exactly** 1<br />[loin:hasObject](hasobject) (op) **min** 1<br />[loin:hasProvider](hasprovider) (op) **exactly** 1<br />[loin:hasPurpose](haspurpose) (op) **exactly** 1<br />
In domain of |[loin:hasProvider](hasprovider) (op)<br />[loin:hasPurpose](haspurpose) (op)<br />[loin:hasObject](hasobject) (op)<br />[loin:hasReceiver](hasinformationreceiver) (op)<br />[loin:isRelatedToContainerDescription](isrelatedtocontainerdescription) (op)<br />
### Information provider
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#InformationProvider`
Description | <p>Information provider is a party for information delivery according to ISO 19650-1 (2018)</p>
Super-classes |[loin:Actor](Actor) (c)<br />
In range of |[loin:hasProvider](hasprovider) (op)<br />
### Information receiver
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#InformationReceiver`
Description | <p>Information receiver is a party for information delivery according to ISO 19650-1 (2018)</p>
Super-classes |[loin:Actor](Actor) (c)<br />
In range of |[loin:hasReceiver](hasinformationreceiver) (op)<br />
### Location
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#Location`
Description | <p>Location as a geometrical information specification for information need according to BS EN 17412-1 (2020)</p>
Super-classes |[loin:GeometrySpecification](Geometricalinformationspecification) (c)<br />
In range of |[loin:hasLocation](haslocation) (op)<br />
### Material
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#Material`
Description | <p>Material is an IDS facet according to IDS developed by buildingSMART International</p>
Super-classes |[loin:IDSFacetDefinition](IDSfacetDefinition) (c)<br />
In domain of |[loin:hasValue](hasvalue) (op)<br />
### Object
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#Object`
Description | <p>Object is a contextual aspect according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Restrictions |[loin:hasInformation](hasalphanumericalinformation) (op) **max** 1<br />[loin:hasDocumentation](hasdocumentation) (op) **max** 1<br />[loin:hasGeometry](hasgeometricalinformation) (op) **max** 1<br />
In domain of |[loin:hasDocumentation](hasdocumentation) (op)<br />[loin:hasGeometry](hasgeometricalinformation) (op)<br />[loin:hasInformation](hasalphanumericalinformation) (op)<br />
In range of |[loin:hasObject](hasobject) (op)<br />
### Ontology data definition
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#OntologyDataDefinition`
Description | <p>Ontology data definition is used to specify the alphanumerical information according to a published or customized ontology</p>
Super-classes |[loin:InformationContent](Alphanumericalinformationcontent) (c)<br />
Restrictions |[loin:specifiedByIdentifier](specifiedbyidentifier) **min** 1<br />
### Parametric behaviour
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#ParametricBehaviour`
Description | <p>Parametric behaviour as a geometrical information specification for information need according to BS EN 17412-1 (2020)</p>
Super-classes |[loin:GeometrySpecification](Geometricalinformationspecification) (c)<br />
In range of |[loin:hasParametricBehaviour](hasparametricbehaviour) (op)<br />
### Predefined type
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#PredefinedType`
Description | <p>Predefined type must be a valid predefined type from the IFC schema, or any custom text value according to IDS developed by buildingSMART International</p>
Super-classes |[loin:IDSFacetParameter](IDSfacetparameter) (c)<br />
Restrictions |[loin:hasRestrictionType](hasrestrictiontype) (op) **exactly** 1<br />
In range of |[loin:hasPredefinedType](haspredefinedtype) (op)<br />
### Property
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#Property`
Description | <p>Property is an IDS facet according to IDS developed by buildingSMART International</p>
Super-classes |[loin:IDSFacetDefinition](IDSfacetDefinition) (c)<br />
Restrictions |[loin:hasIFCDataType](hasIFCdatatype) (op) **exactly** 1<br />[loin:hasPropertyName](haspropertyname) (op) **exactly** 1<br />[loin:belongsToPset](belongstoPset) (op) **exactly** 1<br />
In domain of |[loin:hasIFCDataType](hasIFCdatatype) (op)<br />[loin:hasPropertyName](haspropertyname) (op)<br />[loin:hasValue](hasvalue) (op)<br />[loin:belongsToPset](belongstoPset) (op)<br />
### Property name
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#PropertyName`
Description | <p>Property name must be a valid name from the IFC schema, or any custom text value according to IDS developed by buildingSMART International</p>
Super-classes |[loin:IDSFacetParameter](IDSfacetparameter) (c)<br />
Restrictions |[loin:hasRestrictionType](hasrestrictiontype) (op) **value** [loin:SimpleValue](http://www.inf.bi.rub.de/loin/ns#SimpleValue) (c)<br />[loin:RestrictionFormulation](RestrictionFormulation) (dp) **exactly** 1<br />
In range of |[loin:hasPropertyName](haspropertyname) (op)<br />
### Property set name
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#PsetName`
Description | <p>Property set name must be a valid name from the IFC schema, or any custom text value according to IDS developed by buildingSMART International</p>
Super-classes |[loin:IDSFacetParameter](IDSfacetparameter) (c)<br />
Restrictions |[loin:hasRestrictionType](hasrestrictiontype) (op) **exactly** 1<br />[loin:RestrictionFormulation](RestrictionFormulation) (dp) **exactly** 1<br />
In range of |[loin:belongsToPset](belongstoPset) (op)<br />
### Purpose
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#Purpose`
Description | <p>Purpose is a contextual aspect according to BS EN 17412-1 (2020)</p>
Super-classes |[rdfs:Resource](http://www.w3.org/2000/01/rdf-schema#Resource) (c)<br />
Restrictions |[loin:description](description) (dp) **exactly** 1<br />
In domain of |[loin:isRelatedToContainerDescription](isrelatedtocontainerdescription) (op)<br />
In range of |[loin:hasPurpose](haspurpose) (op)<br />
### Value
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#Value`
Description | <p>Value can be any custom value according to IDS developed by buildingSMART International</p>
Super-classes |[loin:IDSFacetParameter](IDSfacetparameter) (c)<br />
Restrictions |[loin:RestrictionFormulation](RestrictionFormulation) (dp) **exactly** 1<br />[loin:hasRestrictionType](hasrestrictiontype) (op) **exactly** 1<br />
In range of |[loin:hasValue](hasvalue) (op)<br />

## Object Properties
[belongs to information content](#belongstoinformationcontent),
[belongs to Pset](#belongstoPset),
[has agent](#hasagent),
[has appearance](#hasappearance),
[has applicability](#hasapplicability),
[has attribute name](#hasattributename),
[has breakdown structure](#hasbreakdownstructure),
[has breakdown structure type](#hasbreakdownstructuretype),
[has detail](#hasdetail),
[has dimensionality](#hasdimensionality),
[has document](#hasdocument),
[has documentaton specification](#hasdocumentatonspecification),
[has documentation](#hasdocumentation),
[has entity name](#hasentityname),
[has geometrical information](#hasgeometricalinformation),
[has geometrical information specification](#hasgeometricalinformationspecification),
[has IFC data type](#hasIFCdatatype),
[has identification](#hasidentification),
[has identifier](#hasidentifier),
[has identifier type](#hasidentifiertype),
[has alphanumerical information](#hasalphanumericalinformation),
[has alphanumerical informaton content](#hasalphanumericalinformatoncontent),
[has location](#haslocation),
[has object](#hasobject),
[has parameter value](#hasparametervalue),
[has parametric behaviour](#hasparametricbehaviour),
[has predefined type](#haspredefinedtype),
[has property name](#haspropertyname),
[has provider](#hasprovider),
[has purpose](#haspurpose),
[has information receiver](#hasinformationreceiver),
[has reference source](#hasreferencesource),
[has requirement](#hasrequirement),
[has requirement type](#hasrequirementtype),
[has restriction type](#hasrestrictiontype),
[has value](#hasvalue),
[is related to container description](#isrelatedtocontainerdescription),
[is related to container document](#isrelatedtocontainerdocument),
[is related to container linkset](#isrelatedtocontainerlinkset),
[is related to Loin document](#isrelatedtoLoindocument),
[](belongstoinformationcontent)
### belongs to information content
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#belongsToInformationContent`
Domain(s) |[loin:Document](Document) (c)<br />
Range(s) |[loin:InformationContent](Alphanumericalinformationcontent) (c)<br />
[](belongstoPset)
### belongs to Pset
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#belongsToPset`
Domain(s) |[loin:Property](Property) (c)<br />
Range(s) |[loin:PsetName](Propertysetname) (c)<br />
[](hasagent)
### has agent
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#hasAgent`
Description | Information of the information delivery actor defined by foaf ontology mit class foaf:Agent
Domain(s) |[loin:Actor](Actor) (c)<br />
[](hasappearance)
### has appearance
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#hasAppearance`
Range(s) |[loin:Appearance](Appearance) (c)<br />
[](hasapplicability)
### has applicability
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#hasApplicability`
Description | The object property describes the applicability of a facet for the specification
Domain(s) |[loin:IDSDataDefinition](IDSdatadefinition) (c)<br />
Range(s) |[loin:IDSFacetDefinition](IDSfacetDefinition) (c)<br />
[](hasattributename)
### has attribute name
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#hasAttributeName`
Domain(s) |[loin:Attribute](Attribut) (c)<br />
Range(s) |[loin:AttributeName](Attributename) (c)<br />
[](hasbreakdownstructure)
### has breakdown structure
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#hasBreakdownStructure`
Domain(s) |[loin:Identification](Identification) (c)<br />
Range(s) |[loin:BreakdownStructure](Breakdownstructure) (c)<br />
[](hasbreakdownstructuretype)
### has breakdown structure type
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#hasBreakdownStructureType`
Domain(s) |[loin:BreakdownStructure](Breakdownstructure) (c)<br />
Range(s) |[loin:BreakdownStructureType](Breakdownstructuretype) (c)<br />
[](hasdetail)
### has detail
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#hasDetail`
Range(s) |[loin:Detail](Detail) (c)<br />
[](hasdimensionality)
### has dimensionality
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#hasDimensionality`
Range(s) |[loin:Dimensionality](Dimensionality) (c)<br />
[](hasdocument)
### has document
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#hasDocument`
Domain(s) |[loin:Documentation](Documentation) (c)<br />
[](hasdocumentatonspecification)
### has documentaton specification
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#hasDocumentSpecification`
Domain(s) |[loin:Document](Document) (c)<br />
Range(s) |[loin:DocumentSpecification](Documentspecification) (c)<br />
[](hasdocumentation)
### has documentation
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#hasDocumentation`
Domain(s) |[loin:Object](Object) (c)<br />
Range(s) |[loin:Documentation](Documentation) (c)<br />
[](hasentityname)
### has entity name
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#hasEntityName`
Domain(s) |[loin:Entity](Entity) (c)<br />
Range(s) |[loin:EntityName](Entityname) (c)<br />
[](hasgeometricalinformation)
### has geometrical information
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#hasGeometry`
Domain(s) |[loin:Object](Object) (c)<br />
Range(s) |[loin:Geometry](Geometricalinformation) (c)<br />
[](hasgeometricalinformationspecification)
### has geometrical information specification
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#hasGeometrySpecification`
Description | ["Appearance", "Detail", "Dimensionality", "Location", "ParametricBehaviour"]
Domain(s) |[loin:Geometry](Geometricalinformation) (c)<br />
Range(s) |[loin:GeometrySpecification](Geometricalinformationspecification) (c)<br />
[](hasIFCdatatype)
### has IFC data type
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#hasIFCDataType`
Domain(s) |[loin:Property](Property) (c)<br />
Range(s) |[loin:IFCDataType](IFCdatatype) (c)<br />
[](hasidentification)
### has identification
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#hasIdentification`
Domain(s) |[loin:Information](Alphanumericalinformation) (c)<br />
Range(s) |[loin:Identification](Identification) (c)<br />
[](hasidentifier)
### has identifier
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#hasIdentifier`
Domain(s) |[loin:BreakdownStructure](Breakdownstructure) (c)<br />
Range(s) |[loin:Identifier](Identifier) (c)<br />
[](hasidentifiertype)
### has identifier type
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#hasIdentifierType`
Domain(s) |[loin:Identifier](Identifier) (c)<br />
Range(s) |[loin:IdentifierType](Identifiertype) (c)<br />
[](hasalphanumericalinformation)
### has alphanumerical information
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#hasInformation`
Domain(s) |[loin:Object](Object) (c)<br />
Range(s) |[loin:Information](Alphanumericalinformation) (c)<br />
[](hasalphanumericalinformatoncontent)
### has alphanumerical informaton content
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#hasInformationContent`
Domain(s) |[loin:Information](Alphanumericalinformation) (c)<br />
Range(s) |[loin:InformationContent](Alphanumericalinformationcontent) (c)<br />
[](haslocation)
### has location
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#hasLocation`
Range(s) |[loin:Location](Location) (c)<br />
[](hasobject)
### has object
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#hasObject`
Domain(s) |[loin:InformationDeliveryMilestone](Informationdeliverymilestone) (c)<br />
Range(s) |[loin:Object](Object) (c)<br />
[](hasparametervalue)
### has parameter value
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#hasParameterValue`
[](hasparametricbehaviour)
### has parametric behaviour
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#hasParametricBehaviour`
Range(s) |[loin:ParametricBehaviour](Parametricbehaviour) (c)<br />
[](haspredefinedtype)
### has predefined type
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#hasPredefinedType`
Domain(s) |[loin:Entity](Entity) (c)<br />
Range(s) |[loin:PredefinedType](Predefinedtype) (c)<br />
[](haspropertyname)
### has property name
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#hasPropertyName`
Domain(s) |[loin:Property](Property) (c)<br />
Range(s) |[loin:PropertyName](Propertyname) (c)<br />
[](hasprovider)
### has provider
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#hasProvider`
Domain(s) |[loin:InformationDeliveryMilestone](Informationdeliverymilestone) (c)<br />
Range(s) |[loin:InformationProvider](Informationprovider) (c)<br />
[](haspurpose)
### has purpose
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#hasPurpose`
Domain(s) |[loin:InformationDeliveryMilestone](Informationdeliverymilestone) (c)<br />
Range(s) |[loin:Purpose](Purpose) (c)<br />
[](hasinformationreceiver)
### has information receiver
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#hasReceiver`
Domain(s) |[loin:InformationDeliveryMilestone](Informationdeliverymilestone) (c)<br />
Range(s) |[loin:InformationReceiver](Informationreceiver) (c)<br />
[](hasreferencesource)
### has reference source
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#hasReferenceSource`
Domain(s) |([loin:BreakdownStructure](Breakdownstructure) (c) or [loin:OntologyDataDefinition](Ontologydatadefinition) (c))<br />
Range(s) |[xsd:anyURI](http://www.w3.org/2001/XMLSchema#anyURI) (c)<br />[owl:Thing](http://www.w3.org/2002/07/owl#Thing) (c)<br />
[](hasrequirement)
### has requirement
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#hasRequirement`
Domain(s) |[loin:IDSDataDefinition](IDSdatadefinition) (c)<br />
Range(s) |[loin:IDSFacetDefinition](IDSfacetDefinition) (c)<br />
[](hasrequirementtype)
### has requirement type
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#hasRequirementType`
Domain(s) |[loin:IDSFacetDefinition](IDSfacetDefinition) (c)<br />
Range(s) |[loin:IDSRequirementType](IDSrequirementtype) (c)<br />
[](hasrestrictiontype)
### has restriction type
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#hasRestrictionType`
Domain(s) |[loin:IDSFacetParameter](IDSfacetparameter) (c)<br />
Range(s) |[loin:IDSRestrictionType](Restrictiontype) (c)<br />
[](hasvalue)
### has value
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#hasValue`
Domain(s) |[loin:Material](Material) (c)<br />[loin:Property](Property) (c)<br />[loin:Attribute](Attribut) (c)<br />
Range(s) |[loin:Value](Value) (c)<br />
[](isrelatedtocontainerdescription)
### is related to container description
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#isRelatedToContainerDescription`
Domain(s) |[loin:Purpose](Purpose) (c)<br />[loin:InformationDeliveryMilestone](Informationdeliverymilestone) (c)<br />
Range(s) |[Container:ContainerDescription](https://standards.iso.org/iso/21597/-1/ed-1/en/Container#ContainerDescription) (c)<br />
[](isrelatedtocontainerdocument)
### is related to container document
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#isRelatedToContainerDocument`
Domain(s) |[loin:Document](Document) (c)<br />
Range(s) |[Container:Document](https://standards.iso.org/iso/21597/-1/ed-1/en/Container#Document) (c)<br />
[](isrelatedtocontainerlinkset)
### is related to container linkset
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#isRelatedToContainerLinkset`
Domain(s) |[loin:Document](Document) (c)<br />
Range(s) |[Container:Linkset](https://standards.iso.org/iso/21597/-1/ed-1/en/Container#Linkset) (c)<br />
[](isrelatedtoLoindocument)
### is related to Loin document
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#isRelatedToLoinDocument`
Domain(s) |[loin:InformationContent](Alphanumericalinformationcontent) (c)<br />
Range(s) |[loin:Document](Document) (c)<br />

## Datatype Properties
[RestrictionFormulation](#RestrictionFormulation),
[description](#description),
[requested](#requested),
[value](#value),
[](RestrictionFormulation)
### RestrictionFormulation
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#RestrictionFormulation`
Domain(s) |[loin:IDSFacetParameter](IDSfacetparameter) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](description)
### description
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#description`
Domain(s) |([loin:InformationContent](Alphanumericalinformationcontent) (c) or [loin:Purpose](Purpose) (c))<br />
[](requested)
### requested
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#requested`
Domain(s) |[loin:Geometry](Geometricalinformation) (c)<br />[loin:Information](Alphanumericalinformation) (c)<br />[loin:GeometrySpecification](Geometricalinformationspecification) (c)<br />
Range(s) |[xsd:boolean](http://www.w3.org/2001/XMLSchema#boolean) (c)<br />
[](value)
### value
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#value`

## Annotation Properties
[Description](#Description),
[name](#name),
[](Description)
### Description
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#Description`
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](name)
### name
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#name`
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />

## Properties
[is related to container party](#isrelatedtocontainerparty),
[is related to linkset identifier](#isrelatedtolinksetidentifier),
[specified by identifier](#specifiedbyidentifier),
[](isrelatedtocontainerparty)
### is related to container party
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#isRelatedToContainerParty`
Domain(s) |[loin:Actor](Actor) (c)<br />
Range(s) |[Container:Party](https://standards.iso.org/iso/21597/-1/ed-1/en/Container#Party) (c)<br />
[](isrelatedtolinksetidentifier)
### is related to linkset identifier
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#isRelatedToLinksetIdentifier`
Domain(s) |[loin:IdentifierType](Identifiertype) (c)<br />
Range(s) |[Linkset:Identifier](https://standards.iso.org/iso/21597/-1/ed-1/en/Linkset#Identifier) (c)<br />
[](specifiedbyidentifier)
### specified by identifier
Property | Value
--- | ---
IRI | `http://www.inf.bi.rub.de/loin/ns#specifiedByIdentifier`
Domain(s) |[loin:InformationContent](Alphanumericalinformationcontent) (c)<br />
Range(s) |[loin:Identifier](Identifier) (c)<br />

## Named Individuals
## Namespaces
* **default (:)**
  * `http://www.inf.bi.rub.de/loin/ns#`
* **Container**
  * `https://standards.iso.org/iso/21597/-1/ed-1/en/Container#`
* **Linkset**
  * `https://standards.iso.org/iso/21597/-1/ed-1/en/Linkset#`
* **dc**
  * `http://purl.org/dc/terms/`
* **foaf**
  * `http://xmlns.com/foaf/0.1#`
* **loin**
  * `http://www.inf.bi.rub.de/loin/ns#`
* **owl**
  * `http://www.w3.org/2002/07/owl#`
* **prov**
  * `http://www.w3.org/ns/prov#`
* **rdf**
  * `http://www.w3.org/1999/02/22-rdf-syntax-ns#`
* **rdfs**
  * `http://www.w3.org/2000/01/rdf-schema#`
* **sdo**
  * `https://schema.org/`
* **sh**
  * `http://www.w3.org/ns/shacl#`
* **skos**
  * `http://www.w3.org/2004/02/skos/core#`
* **vann**
  * `http://purl.org/vocab/vann/`
* **xml**
  * `http://www.w3.org/XML/1998/namespace`
* **xsd**
  * `http://www.w3.org/2001/XMLSchema#`

## Legend
* Classes: c
* Object Properties: op
* Functional Properties: fp
* Data Properties: dp
* Annotation Properties: dp
* Properties: p
* Named Individuals: ni