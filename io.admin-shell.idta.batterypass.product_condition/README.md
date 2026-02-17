# Scope

This namespace is reserved for the Submodel Template Specification (SMT)  IDTA-02035-5 Digital Battery Passport - Part 5: Product Condition 

Namespace: urn:samm:io.admin-shell.idta.batterypass.product_condition

The battery passport consists of the following 7 parts:

*	Digital Battery Passport - Part 1: Digital Nameplate (IDTA-02035-1)
*	Digital Battery Passport - Part 2: Handover Documentation (IDTA-02035-2)
*	Digital Battery Passport - Part 3: Product Carbon Footprint  (IDTA-02035-3)
*	Digital Battery Passport - Part 4: Technical Data (IDTA-02035-4) 
*	Digital Battery Passport - Part 5: Product Condition  (IDTA-02035-5)
*	Digital Battery Passport - Part 6: Material Composition  (IDTA-02035-6)
*	Digital Battery Passport - Part 7: Circularity  (IDTA-02035-7)


Source GitHub IDTA for .aasx file and Submodel Template Specification etc.: https://github.com/admin-shell-io/submodel-templates 



# Dependencies





# Changelog
All notable changes to this model will be documented in this section.

## [1.0.0] - February 2026

for changelog see  [IDTA-02035-5 V1.2, section "Version history"]()

Contained Files:

* ProductCondition.ttl
* ProductCondition_shared.ttl (extract from BatteryPass Consortium)
* Namespace.ttl



Dependencies:

* urn:samm:io.admin-shell.idta.handover_documentation:2.0.0
* urn:samm:io.admin-shell.idta.shared:3.1.0


Deviations:
* informationOnAccidents is modelled as a Set of Document Identifier (reuse from SMT HandoverDocumentation), in DIN DKE SPEC 99100 it is described as a Reference to a pdf File.  

## ECLASS

no ECLASS IRDIs for

* NegativeEvents
* SMC TemperatureInformation (but for temperatures within)
* EvolutionOfSelfDischarge
* CurrentSelfDischargingRate