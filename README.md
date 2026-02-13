# Legal Note

Despite great efforts to ensure the accuracy, reliability and precision of technical and non-technical information, the IDTA cannot give any explicit or implicit assurance or warranty in respect of the accuracy of the provided aspect models for BatteryPass. 
Users of this document are hereby made aware that the IDTA cannot be held liable for any damage or loss. 
The application of these aspect models does not release users from the bility for their own actions and is applied at their own risk.

# Semantic Models


This repository is for semantic models based on the [ESMF](https://eclipse-esmf.github.io/esmf-documentation/index.html) [Semantic Aspect Meta Model (SAMM)](https://eclipse-esmf.github.io/samm-specification) .

There are differnt ways how to create and use these Aspect Models in [Submodel Template Specifications](https://github.com/admin-shell-io/submodel-templates):

* They are used as master of the semantic definitions used in the so-called "Semantic Drived workflow" as desribed in [HOW TO CREATE A SUBMODEL TEMPLATE
SPECIFICATION](https://industrialdigitaltwin.org/en/wp-content/uploads/sites/2/2022/12/I40-IDTA-WS-Process-How-to-write-a-SMT-FINAL-.pdf)
* They are created on basis of an existing Submodel Template Specification
* They are build parallel to a Submodel Template Specification using a different workflow or using different semantic definitions as master
* They are build for reuse but no Submodel Template Specification is existing for these


[Best practices](https://eclipse-esmf.github.io/samm-specification/snapshot/appendix/best-practices.html) as defined in the SAMM specification should be followed.

When creating an Aspect Model for an existing Submodel Template Specification it is recommended to use the predefined Characteristics in [io.admin-shell.idta.shared](https://github.com/admin-shell-io/smt-semantic-models/tree/main/io.admin-shell.idta.shared) to ensure that [Value-Only](https://industrialdigitaltwin.io/aas-specifications/IDTA-01001/v3.1.2/mappings/mappings.html#value-only-serialization-in-json)  format of AAS is identical to the  [payload](https://eclipse-esmf.github.io/samm-specification/snapshot/payloads.html) as defined by SAMM.

The Aspect Models defined in this repository belong to the [namespaces](https://eclipse-esmf.github.io/samm-specification/snapshot/namespaces.html) starting with *io.admin-shell.idta*.


Models can reuse elements from different namespaces within the repository.

When defining and reusing elements from other aspect models, the following repositories with aspect models are allowed to be used besides the ones in this repository:

* [Catena-X aspect models](https://github.com/eclipse-tractusx/sldt-semantic-models), their namespaces start with *io.catenax*
* [BatteryPass aspect models](https://github.com/batterypass/BatteryPassDataModel), their namespaces start with *io.BatteryPass* - however, please note that older version of these aspect models have licence **CC BY-NC 4.0**, only use Aspect Models with licence **CC BY 4.0**


# Generator used

The following [CLI - Semantic Aspect Meta Model Command Line Tool](https://eclipse-esmf.github.io/esmf-developer-guide/tooling-guide/samm-cli.html) was used for

* validating the aspect models
* for generating the different files in folder "gen"

>   ***-schema.json**  JSON schema for [Value-Only](https://industrialdigitaltwin.io/aas-specifications/IDTA-01001/v3.1.2/mappings/mappings.html#value-only-serialization-in-json) format of AAS
> 
>   ***.json**  example payload in [Value-Only format](https://industrialdigitaltwin.io/aas-specifications/IDTA-01001/v3.1/mappings/mappings.html#value-only-serialization-in-json) conformant to generated schema *-schema.json*
> 
>   ***.html**  hmtl documentation of the Aspect Model

The corresponding commands with **%1** being the .ttl with the Aspect Model and **%2** is the name of the file, typically the name of the Aspect Model, are

>samm aspect %1 validate
>
>samm aspect %1 to json --output "../_gen/%2.json"
>
> samm aspect %1 to schema  --output "../_gen/%2-schema.json"



The following version of the **samm-cli - Semantic Aspect Meta Model Command Line Tool** was used for validation and generation:


 > Version: 2.13.1
>   
 > Build date: 2026-01-19 14:02:48
> 
 > Git commit: 047a17acdf0c1ecd945b671c0da45657bea87678


The following version of the [Semantic Aspect Meta Model (SAMM)](https://eclipse-esmf.github.io/samm-specification) is currently used: 

> **2.2.0**




