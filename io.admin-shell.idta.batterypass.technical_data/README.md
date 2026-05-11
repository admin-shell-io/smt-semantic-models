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


- optional ProductClassifications not included
- optional FurtherInformation not included
- optional SpecificDescriptions not included
- Newly added properties to GeneralInformation
  * ManufacturerIdentifier
  * WarrantyInformation
  * BatteryCategory
  * BatteryMass
* Properties of GeneralInformation not included
 - mandatory manufacturerProductDesignation not included (similar to Digital Nameplate)
 - mandatory manufacturerArticleNumber not included (similar to Digital Nameplate)
 - mandatory manufacturerOrderCode not included (similar to Digital Nameplate)

- TechnicalPropertyAreas not realized as SML but as SMC (https://github.com/admin-shell-io/submodel-templates/issues/175[#175])

# Changelog
All notable changes to this model will be documented in this section.

## [1.0.1] - April 2026

Major Changes:

* DELETED: remove properties ManufacturerProductDesignation, ManufacturerArticleNumber and ManufacturerOrderCode (https://github.com/admin-shell-io/smt-semantic-models/issues/82[#82])
* CHANGED: data type of WarrantyPeriod changed to xsd:string with regex constraint conformant to ISO 8601 duration format (https://github.com/admin-shell-io/smt-semantic-models/issues/89[#89])
* CHANGE: WarrantyPeriod now property of entity WarrantyInformation, within GenerationInformation WarrantyPeriod substituted by WarrantyInformation (https://github.com/admin-shell-io/smt-semantic-models/issues/89[#89])
* CHANGE: add IRDI to :TechnicalAttributes to be compliant to IDTA-02003-2-0 Generic Technical Data 2.0.1 (https://github.com/admin-shell-io/smt-semantic-models/issues/88[#88])

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

# Known Deviations from DIN DKE SPEC 99100

Cycle-life Reference test is not of type "string" but references a (pdf) document, realized as set of document identifiers

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



