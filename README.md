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


# Generator used

[samm-cli - Semantic Aspect Meta Model Command Line Tool](https://github.com/eclipse-esmf/esmf-sdk)
Version: 2.10.3
Build date: 2025-05-08T14:47:57Z
Git commit: 192116d12a1a4c9df4e03758a6b56dfa80132cf3

# Known Issues generation of aasx from aspect model

Known Issues wehen generating an aasx from aspect model:

- payload names are not considered when generating idShort
- SubmodelElement File is realized as SMC with two properties
- no template qualifiers with type "Cardinality" or any other qualifiers are generated
- the idShort of the Element within a SML has the idShort of the list, not of the element
- no mapping to SubmodelElement "File", instead mapping to SMC with two properties "resourceValue" and "contentType"


# Open Questions

* PowerCapabilityFade was removed from Technical Data? It belonged to Capacity before


# Deviations from manually edited aasx of WG

* ProductCondition
  * batteryStatus missing
  * "lastUpdate" property for the properties that change over time
* Nameplate 3.0 should be used, not 2.0
	* Nameplate: it is AddressInformation and not ContactInformation
	* Nameplate: logoCompany is missing
	* Naemplate/Markings: explosionSafeties not  contained in V3.0 any longer
	* Nameplate/ContactInformation: is a dropin and contains much more properties
	
* TODOs for BatteryPass reused

    * remainingEnergy: property name should be remainingEnergyValue and not remainingEnergyvalue
	* why is evolutionOfSelfDischarge a SMC with just one Property evolutionOfSelfDischargeEntityValue?
	* names of lists like "internalResistanceIncrease" or remainingPowerCapability
    * no "lastUpdate" for batteryStatus
    * no "lastUpdate" for energyThroughput
	* no "lastUpdate" for roundTripEfficencyFade
	* no "lastUpdate" for roundTripEfficiencyat50PerCentCycleLife 
	* naming roundTripEfficiencyat50PerCentCycleLife should be roundTripEfficiencyAt50PercentCycleLife