
# Open Questions

* PowerCapabilityFade was removed from Technical Data? It belonged to Capacity before


## Deviations from manually edited aasx of WG

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
	
## TODOs for BatteryPass reused

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
	
## Circularity

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
		 
## Other	
 
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