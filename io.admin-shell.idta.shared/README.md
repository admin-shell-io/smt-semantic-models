# Scope

This namespace is reserved for shared elements used in several aspect models and Submodel Templates

Namespace: urn:samm:io.admin-shell.idta.shared

# General

The folder "gen" for each version contains sammple JSON files generated for the aspect model(s)
The folder "input" contains source files like .aasx or the submodel template specification itself

# Changelog
All notable changes to this model will be documented in this section.

## [3.1.0] - May 2025 based on IDTA-01001-3-1 Specifications of the Asset Administration Shell: Metamodel

for detailled changelog see [IDTA-01001-3-1](https://industrialdigitaltwin.io/aas-specifications/IDTA-01001/v3.1)

Contained Files:

The following shared files ensure that  [Value-Only serialization](https://industrialdigitaltwin.io/aas-specifications/IDTA-01001/v3.1/mappings/mappings.html#value-only-serialization-in-json) is consistent to the specification in [IDTA-01001-3-1](https://industrialdigitaltwin.io/aas-specifications/IDTA-01001/v3.1)

* Entity_shared.ttl: Characteristic used for properties of submodel element type [Entity](https://industrialdigitaltwin.io/aas-specifications/IDTA-01001/v3.1/spec-metamodel/submodel-elements.html#entity-attributes). Dependency to SpecificAssetId_shared.ttl
* File_shared.ttl: Characteristic used for properties of submodel element type [File](https://industrialdigitaltwin.io/aas-specifications/IDTA-01001/v3.1/spec-metamodel/submodel-elements.html#file-attributes)
* Blob_shared.ttl: Characteristic used for properties of submodel element type [Blob](https://industrialdigitaltwin.io/aas-specifications/IDTA-01001/v3.1/spec-metamodel/submodel-elements.html#blob-attributes)
* contentType_shared.ttl: property "contentType" used in submodel element types File and Blob
* MultiLanguageTexts_shared.ttl: Characteristic used for properties of submodel element type [MultiLanguageProperty](https://industrialdigitaltwin.io/aas-specifications/IDTA-01001/v3.1/spec-metamodel/submodel-elements.html#_multi_language_property_attributes)
* Reference_shared.ttl: Characteristic used for attributes/SAMM properties of submodel element type [Reference](https://industrialdigitaltwin.io/aas-specifications/IDTA-01001/v3.1/spec-metamodel/referencing.html#_reference_attributes]) 
* RelationshipElement_shared.ttl: Characteristic for properties of submodel element type [RelationshipElement](https://industrialdigitaltwin.io/aas-specifications/IDTA-01001/v3.1/spec-metamodel/submodel-elements.html#relationship-element-attributes)
* SpecificAssetId_shared.ttl: Characteristic used for [specificAssetId](https://industrialdigitaltwin.io/aas-specifications/IDTA-01001/v3.1/spec-metamodel/core.html#specific-asset-id-attributes) as used for example as attribute type in submodel element type [Entity](https://industrialdigitaltwin.io/aas-specifications/IDTA-01001/v3.1/spec-metamodel/submodel-elements.html#entity-attributes)

Additionally, properties are predefined that may be used in several Submodel Templates:

* Markings_shared: properties for markings as used for example in SMT "Nameplate"
* languageSet_shared: property "languages" for a set of languages

Two aspect model are contained to illustrate how to use the properties and characteristics, they are exemplary only:

* ValueOnlyExampleAspect.ttl: shows how to use the characteristics for different submodel element types
* TestAspect.ttl: shows how to use predefined properties

Dependencies:

NONE


In the following only deviations from IDTA-01001-3-1 are documented:

NONE