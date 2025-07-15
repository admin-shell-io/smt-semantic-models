# Semantic Models

This repository is for aspect models that are used as semantic definition in [Submodel Templates](https://github.com/admin-shell-io/submodel-templates).

They are used in the so-called "Semantic driven workflow" as desribed in [HOW TO CREATE A SUBMODEL TEMPLATE
SPECIFICATION](https://industrialdigitaltwin.org/wp-content/uploads/2025/06/IDTA_How-to-write-a-SMT-v1.1.pdf).

Here semantic models based on the [Semantic Aspect Meta Model (SAMM)](https://eclipse-esmf.github.io/samm-specification) are stored. 
Additionally, [best practices](https://eclipse-esmf.github.io/samm-specification/snapshot/appendix/best-practices.html) as defined in the SAMM specification should be followed.

They belong to the namespaces starting with **io.admin-shell.idta**.

Models can reuse elements from different namespaces within the repository.

When defining and reusing elements from other aspect models, the following repositories with aspect models are allowed to be used besides the ones in this repository:

* [Catena-X aspect models](https://github.com/eclipse-tractusx/sldt-semantic-models), their namespaces start with *io.catenax*
* [BatteryPass aspect models](https://github.com/batterypass/BatteryPassDataModel), their namespaces start with *io.BatteryPass* - however, please note that these aspect models have licence **CC BY-NC 4.0**.


