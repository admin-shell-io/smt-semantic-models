# Scope

This namespace is reserved for the Submodel Template Specification (SMT) [IDTA-02003 Generic Frame for Technical Data for Industrial Equipment in Manufacturing](https://industrialdigitaltwin.org/wp-content/uploads/2022/10/IDTA-02003-1-2_Submodel_TechnicalData.pdf)

Namespace: urn:samm:io.admin-shell.idta.generic.technical_data

# General

The folder "gen" for each version contains sammple JSON files generated for the aspect model(s)
The folder "input" contains source files like .aasx or the submodel template specification itself

# Changelog
All notable changes to this model will be documented in this section.

## [1.2.0] - 2005-03-11

Contained Files:

* TechnicalData.ttl: the aspect model for the SMT : the _see_ attribute needs to be extended to include the ID of the concrete technical data SMT derived from this generic SMT

* furtherInformation_generic.ttl : this file needs to be substituted when deriving a concrete techncial data SMT from this generic SMT
* technicalProperties_generic.ttl : this file needs to be substituted when deriving a concrete techncial data SMT from this generic SMT
* generalInformation_shared.ttl : as defined in SMT IDTA-02003, probably to be substituted by the entity in generalInformation_nameplate_shared.ttl
* generalInformation_nameplate_shared.ttl  : this file is identical to generalInformation_shared but reused the corresponding properties form SMT Nameplate 3.0.0
* productImages_shared.ttl : property for a set of product images
* productClassifications_shared.ttl


Dependencies:

* urn:samm:io.admin-shell.idta.nameplate:3.0.0#   - if generalInformation_nameplate_shared.ttl is used
* urn:samm:io.admin-shell.idta.shared:3.1.0#


In the following only deviations from IDTA-02003-3-0 are documented:

### Added

* add some German preferred names or descriptions

		
### Changed

* properties from Nameplate were used for SMC _GeneralInformation_ except for the new _productImage_ and payload name was adapted if differing from SMT Digital Nameplate 3.0
* _ProductImage_ was mapped to a SAMM property _productImages_ since it is 0..*. The semanticId was changed  from https://admin-shell.io/ZVEI/TechnicalData/ProductImage/1/1 to ]https://admin-shell.io/ZVEI/TechnicalData/ProductImages/1/1


### Removed

--


### Example for Usage

Technical Data is a generic template, i.e. it not intended for data exchange as is. The properties for the technical data need to be added.

This is how a specific technical data SMT can be created based on this generic one:

file "TechnicalData.ttl" with the aspect. The aspect has the same name as the original one. This file can just be copied without any change. In this case the property "furtherInformation" is omitted since it is optional and not needed for this example.

```
@prefix samm: <urn:samm:org.eclipse.esmf.samm:meta-model:2.1.0#> .
@prefix samm-c: <urn:samm:org.eclipse.esmf.samm:characteristic:2.1.0#> .
@prefix samm-e: <urn:samm:org.eclipse.esmf.samm:entity:2.1.0#> .
@prefix unit: <urn:samm:org.eclipse.esmf.samm:unit:2.1.0#> .
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .
@prefix : <urn:samm:io.admin-shell.idta.technical_data.example:1.0.0#> .
@prefix generic: <urn:samm:io.admin-shell.idta.generic.technical_data:1.0.0#> .
@prefix nameplate: <urn:samm:io.admin-shell.idta.digital_nameplate:3.0.0#> .
@prefix samm-u: <urn:samm:org.eclipse.esmf.samm:unit:2.1.0#> .
@prefix shared: <urn:samm:io.admin-shell.idta.shared:3.1.0#> .

:TechnicalData a samm:Aspect ;
   samm:preferredName "technical properties"@en ;
   samm:description "Technical data of the Battery Pass."@en ;
   samm:see <https://admin-shell.io/ZVEI/TechnicalData/Submodel/1/2> ;
   samm:properties ( :technicalProperties [ samm:property generic:productClassifications; samm:optional true ] generic:generalInformation ) ;
   samm:operations ( ) ;
   samm:events ( ) .

:technicalProperties a samm:Property ;
   samm:preferredName "technical properties"@en ;
   samm:description "Technical and product properties. Individual Characteristics that describe the product and its technical properties."@en ;
   samm:see <https://admin-shell.io/ZVEI/TechnicalData/TechnicalProperties/1/1> ;
   samm:characteristic :TechnicalPropertiesCharacteristic .
```

and a second file defining the specific technical properties for the product under consideration. In this example a property "addYourProperty" is added to "technicalProperties" with type "Text".

```
@prefix samm: <urn:samm:org.eclipse.esmf.samm:meta-model:2.1.0#> .
@prefix samm-c: <urn:samm:org.eclipse.esmf.samm:characteristic:2.1.0#> .
@prefix samm-e: <urn:samm:org.eclipse.esmf.samm:entity:2.1.0#> .
@prefix unit: <urn:samm:org.eclipse.esmf.samm:unit:2.1.0#> .
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .
@prefix : <urn:samm:io.admin-shell.idta.technical_data.example:1.0.0#> .
@prefix generic: <urn:samm:io.admin-shell.idta.generic.technical_data:1.0.0#> .
@prefix nameplate: <urn:samm:io.admin-shell.idta.digital_nameplate:3.0.0#> .
@prefix samm-u: <urn:samm:org.eclipse.esmf.samm:unit:2.1.0#> .
@prefix shared: <urn:samm:io.admin-shell.idta.shared:3.1.0#> .

:TechnicalPropertiesCharacteristic a samm-c:SingleEntity ;
   samm:preferredName "technical properties"@en ;
   samm:description "Technical data of the Battery Pass."@en ;
   samm:dataType :TechnicalPropertiesEntity .

:TechnicalPropertiesEntity a samm:Entity ;
   samm:preferredName "technical properties"@en ;
   samm:description "property describing technical capabilities of your product"@en ;
   samm:properties ( :addYourProperty ) .

:addYourProperty  a samm:Property ;
   samm:preferredName "my property"@en ;
   samm:description "technical property of your product"@en ;
   samm:characteristic samm-c:Text ;
   samm:exampleValue "example property value" .

```