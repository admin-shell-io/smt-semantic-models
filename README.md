Despite great efforts to ensure the accuracy, reliability and precision of technical and non-technical information, the IDTA cannot give any explicit or implicit assurance or warranty in respect of the accuracy of the provided aspect models for BatteryPass. 
Users of this document are hereby made aware that the IDTA cannot be held liable for any damage or loss. 
The application of these aspect models does not release users from the bility for their own actions and is applied at their own risk.

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
- Concept Descriptions: For enumerations no valueList is created for its values (example :HazardousSubstanceClassChrateristicEnum in MaterialComposition)


# Open Questions

* PowerCapabilityFade was removed from Technical Data? It belonged to Capacity before


# Deviations from manually edited aasx of WG

* Open Questions:

  * How to deal with different requirements for different battery categories: mandatory, recommended and optional?

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
	* why is evolutionOfSelfDischarge a SMC with just one Property evolutionOfSelfDischargeEntityValue? "lastValue" missing?
	* names of lists like "internalResistanceIncrease" or remainingPowerCapability
    * no "lastUpdate" for batteryStatus
    * no "lastUpdate" for energyThroughput
	* no "lastUpdate" for roundTripEfficencyFade
	* no "lastUpdate" for roundTripEfficiencyat50PerCentCycleLife 
	* naming roundTripEfficiencyat50PerCentCycleLife should be roundTripEfficiencyAt50PercentCycleLife
	* Circularity/safetyMeasures is a Link to a pdf, here it is a SMC with a SML of extinguishingAgents... Extinguishing agent are mentioned in DIN SPEC 99100 but as Symbols/Labels and documentation for conformity
	* Circularity/endOfLifeInformation not part of DIN SPEC 991100 ?
	* Circularity/renewable Content not part of DIN SPEC 991100 ?
	
	* Circulariy/sparePartSources provided both: the part numbers and the adresses, might be splitted or the other way around: start with part number and address (but thenn address may be redundant).
	
* Circularity

	* dismantlinAndRemovalInformation mdoelled as a DocumentSet from Handover Documentation? (it is a SML with SMC with properties documentType, mimeType and documentURL" - we probably need to extend the numbers (or map it to existing ones) of supported document types in Handover Documentation:
	     ** dismantling information(DIN SPEC 99100 speaks of two documents for dismantling and removal)
		 ** removal information (DIN SPEC 99100 speaks of two documents for dismantling and removal)
		 ** safety measures
		 ** Information of due diligence report in the Battery Passport
		 EU declaration of conformity
		 Results of test reports proving compliance
		 Web link to public carbon footprint study
		 Information of due diligence report in the Battery Passport
		 Information on the role of end-users in contributing to waste prevention
		 Information on the role of end-users in contributing to the separate collection of waste batteries
		 Information on battery collection, preparation for second life and on treatment at end of life
		 
		 
* license information not put to description but to README

* formatting in case of lists in descriptions etc.: rework needed

* DIN SPEC 99100: why is Part Numbers for components an URL?
* Circularity/sparePartSources might be using contactInformation for Postal Addresses
* do we have a SMT for spare parts?

* TO BE DECIDED:
  DocumentSet per aspect, for Circularity etc. - or really in ONE aspect Handover Documentation?
  
* unit in SAMM - define a "real" unit?
		:kilogramperkilowatthour a samm:Unit ;
		   samm:commonCode "kg CO2e/kWh" ;
		   samm:symbol "CO2e/kWh" .