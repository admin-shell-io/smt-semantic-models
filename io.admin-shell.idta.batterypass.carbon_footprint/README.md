# Scope

This namespace is reserved for the Submodel Template Specification (SMT)  IDTA-02035-3 Digital Battery Passport - Part 3: Product Carbon Footprint 

This SMT is derived from IDTA-02023 Version 1.0 Carbon Footprint, urn:samm:io.admin-shell.idta.carbon_footprint:1.0.0#

The battery passport consists of the following 7 parts:

*	Digital Battery Passport - Part 1: Digital Nameplate (IDTA-02035-1)
*	Digital Battery Passport - Part 2: Handover Documentation (IDTA-02035-2)
*	Digital Battery Passport - Part 3: Product Carbon Footprint  (IDTA-02035-3)
*	Digital Battery Passport - Part 4: Technical Data (IDTA-02035-4) 
*	Digital Battery Passport - Part 5: Product Condition  (IDTA-02035-5)
*	Digital Battery Passport - Part 6: Material Composition  (IDTA-02035-6)
*	Digital Battery Passport - Part 7: Circularity  (IDTA-02035-7)


# How to add product or sector specific Carbon Footprints


see IDTA-02023


# Changelog
All notable changes to this model will be documented in this section.

## [1.0.0] - 2025-12

for changelog see  [IDTA-02035-3 V1.0, section "Version history"]()

Contained Files:

* CarbonFootprintBattery.ttl


Dependencies:

@prefix pcf: <urn:samm:io.admin-shell.idta.carbon_footprint:1.0.0#> .
@prefix cx: <urn:samm:io.catenax.pcf:8.0.0#> .
@prefix ext-shared: <urn:samm:io.admin-shell.idta.shared:3.1.0#> .
@prefix contact: <urn:samm:io.admin-shell.idta.contact_information:1.0.0#> .


# Deviations compared to urn:samm:io.admin-shell.idta.carbon_footprint:1.0.0#:
- optional ProductOrSectorSpecificCarbonFootprints from IDTA-02023 not included
- description were updated to include information on DIN DKE SPEC 99110
- not included for Battery Passport:
 
  * :explanatoryStatement
  * :goodsHandoverAddress
  * :publicationDate  (although mandatory)
  * :expirationDate
  * :productOrSectorSpecificCarbonFootprints
  
- new propertiers specific to Battery Passport: 

  * :performanceClass
  * :webLinkToPublicCarbonFootprintStudy

for potential additional deviations see Aspect Model for IDTA-02023, urn:samm:io.admin-shell.idta.carbon_footprint:1.0.0#

# Deviations compared to IDTA-02023 aasx:

for potential additional deviations see Aspect Model for IDTA-02023, urn:samm:io.admin-shell.idta.carbon_footprint:1.0.0#