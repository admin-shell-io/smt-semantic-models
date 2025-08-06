# Legal Note

Despite great efforts to ensure the accuracy, reliability and precision of technical and non-technical information, the IDTA cannot give any explicit or implicit assurance or warranty in respect of the accuracy of the provided aspect models for BatteryPass. 
Users of this document are hereby made aware that the IDTA cannot be held liable for any damage or loss. 
The application of these aspect models does not release users from the bility for their own actions and is applied at their own risk.

# Semantic Models

This repository is for aspect models that are used as semantic definition in [Submodel Templates](https://github.com/admin-shell-io/submodel-templates).

They are used in the so-called "Semantic driven workflow" as desribed in [HOW TO CREATE A SUBMODEL TEMPLATE
SPECIFICATION](https://industrialdigitaltwin.org/wp-content/uploads/2025/06/IDTA_How-to-write-a-SMT-v1.1.pdf).

Here semantic models based on the [Semantic Aspect Meta Model (SAMM)](https://eclipse-esmf.github.io/samm-specification) are stored. 
[Best practices](https://eclipse-esmf.github.io/samm-specification/snapshot/appendix/best-practices.html) as defined in the SAMM specification should be followed.

They belong to the namespaces starting with **io.admin-shell.idta**.

Models can reuse elements from different namespaces within the repository.

When defining and reusing elements from other aspect models, the following repositories with aspect models are allowed to be used besides the ones in this repository:

* [Catena-X aspect models](https://github.com/eclipse-tractusx/sldt-semantic-models), their namespaces start with *io.catenax*
* [BatteryPass aspect models](https://github.com/batterypass/BatteryPassDataModel), their namespaces start with *io.BatteryPass* - however, please note that these aspect models have licence **CC BY-NC 4.0**.


# Generator used

The following [CLI - Semantic Aspect Meta Model Command Line Tool](https://eclipse-esmf.github.io/esmf-developer-guide/tooling-guide/samm-cli.html) was used for

* validating the aspect models
* for generating the different files in folder "gen"

  * *.aas.json JSON format for AAS
  * *.aas.xml  XML format for AAS
  * *.aasx  [aasx format](https://industrialdigitaltwin.io/aas-specifications/IDTA-01005/v3.1/index.html) for AAS
  * *.html  hmtl documentation of the Aspect Model
  * *.json  example payload in [Value-Only format](https://industrialdigitaltwin.io/aas-specifications/IDTA-01001/v3.1/mappings/mappings.html#value-only-serialization-in-json)


Version: 2.10.3

Build date: 2025-05-08T14:47:57Z

Git commit: 192116d12a1a4c9df4e03758a6b56dfa80132cf3


# Known issues for generation of aasx from aspect model

Known Issues wheen generating an aasx file from a .ttl aspect model file:

- payload names are not considered when generating idShort
- no template qualifiers with type "Cardinality" or any other qualifiers are generated
- the idShort of the Element within a SML has the idShort of the list, not of the element
- no mapping to SubmodelElement "File", instead mapping to SMC with two properties "resourceValue" and "contentType"
- no example values generated, neither as "value" nor as qualifier using the template qualifier "SMT/ExampleValue"
- semanticId only added for Properties but not for SMC or SML (but ConceptDescriptions are derived)
- Concept Descriptions: For enumerations no valueList is created for its values (example :HazardousSubstanceClassChrateristicEnum in MaterialComposition)
- Concept Descriptions: The preferred name is identical to the element name and not the samm:preferred name of the samm:property

