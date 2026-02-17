# Scope

This namespace is reserved for the Submodel Template Specification (SMT)  IDTA-02035-4 Digital Battery Passport - Part 4: Technical Data 

This SMT is derived from IDTA-02003-2-0 Generic Technical Data 2.0 

Namespace: urn:samm:io.admin-shell.idta.batterypass.technical_data


The battery passport consists of the following 7 parts:

*	Digital Battery Passport - Part 1: Digital Nameplate (IDTA-02035-1)
*	Digital Battery Passport - Part 2: Handover Documentation (IDTA-02035-2)
*	Digital Battery Passport - Part 3: Product Carbon Footprint  (IDTA-02035-3)
*	Digital Battery Passport - Part 4: Technical Data (IDTA-02035-4) 
*	Digital Battery Passport - Part 5: Product Condition  (IDTA-02035-5)
*	Digital Battery Passport - Part 6: Material Compostion  (IDTA-02035-6)
*	Digital Battery Passport - Part 7: Circularity  (IDTA-02035-7)

Source GitHub IDTA for .aasx file and Submodel Template Specification etc.: https://github.com/admin-shell-io/submodel-templates 


# General

The folder "gen" for each version contains sample JSON files generated for the aspect model(s)

Deviations from IDTA-02003-2-0

- optional productClassifications not included
- optional furtherInformation not included
- optional specificDescriptions not included

- TechnicalPropertyAreas not realized as SML but as SMC (https://github.com/admin-shell-io/submodel-templates/issues/175)

# Changelog
All notable changes to this model will be documented in this section.

## [1.0.0] - February 2026

Contained Files:

* TechnicalData.ttl: the Aspect Model for the SMT 
* technicalProperties_shared.ttl: entities
* technicalProperties_scalar_shared.ttl: scalar properties
* generalInformation_shared.ttl: generalInformation as specified in generic Technical Data
* enum_BatteryCategory_shared.ttl: enumeration for the different categories of batteries
* units.ttl: measurement units specific for battery

# Dependencies:

This model is using  models or model elements of the BatteryPass Consortium: https://github.com/batterypass/BatteryPassDataModel
with license CC BY 4.0. 

@prefix tech: <urn:samm:io.admin-shell.idta.generic.technical_data:2.0.0#> .
@prefix shared: <urn:samm:io.admin-shell.idta.shared:3.1.0#> .
@prefix nameplate: <urn:samm:io.admin-shell.idta.digital_nameplate:3.0.0#> .


# Known Deviations from IDTA-02003-2-0

In the following only deviations are documented:

### Added

to GenerationInformation:

* manufacturerIdentifier
* warrantyPeriod
* batteryCategory
* batteryMass

### Changes

the following mandatory elements from IDTA-02003-2-0 are not included:

* manufacturerProductDesignation



