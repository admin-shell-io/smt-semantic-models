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

Source GitHub IDTA: https://github.com/admin-shell-io/submodel-templates 
Source Content Hub of the IDTA: [IDTA-02035-4 V2.0]()

# General

The folder "gen" for each version contains sample JSON files generated for the aspect model(s)

Deviations from IDTA-02003-2-0

- optional productClassifications not included
- optional furtherInformation not included
- optional specificDescriptions not included

- TechnicalPropertyAreas not realized as SML but as SMC (https://github.com/admin-shell-io/submodel-templates/issues/175)

# Changelog
All notable changes to this model will be documented in this section.

## [1.0.0] - add date

Contained Files:

* TechnicalData.ttl: the aspect model for the SMT 
* technicalProperties_shared.ttl
* technicalProperties_scalar_shared.ttl
* generalInformation_shared.ttl

# Dependencies:

This model is using  models or model elements of the BatteryPass Consortium: https://github.com/batterypass/BatteryPassDataModel
with license CC BY 4.0. 

@prefix tech: <urn:samm:io.admin-shell.idta.generic.technical_data:2.0.0#> .
@prefix shared: <urn:samm:io.admin-shell.idta.shared:3.1.0#> .
@prefix nameplate: <urn:samm:io.admin-shell.idta.digital_nameplate:3.0.0#> .
@prefix bp: <urn:samm:io.BatteryPass.Performance:1.2.1#> .
@prefix bpg: <urn:samm:io.BatteryPass.GeneralProductInformation:1.2.0#> 

# Known Deviations (IDTA-02003-1-2)

In the following only deviations are documented:

### Added

to GenerationInformation:

* manufacturerIdentifier
* warrantyPeriod
* batteryCategory
* batteryMass

		
### Changed




### Removed




## Deviations

* IRDIs from ECLASS not added in case properties of BatteryPass were reused
* Some descriptions deviate from those in the specification in case properties of BatteryPass were reused
* example values not added in case properties of BatteryPass were reused
* added: missing description for Capacity
* for nominalVoltage, MaxVoltage and MinVoltage the descriptions of BatteryPass were taken
* in BatteryPass PowerCapabilityat20Charge or 80Charge is float and not double
* in BatteryPass originalPowerCapabilityLimits is not existing but PowerCapabilities is float, Characteristic bp:PowerCapabilityAtSoc is used
* ratedEnergy from BatteryPass was used as Characteristic for MaximumAllowedBatteryEnergy, but is float, in .docs it is double
* maximumPermittedBatteryPower and originalPowerCapabilityLimits uses bp:PowerCapabilityAtSoc and thus is float and not double
* maximumAllowedBatteryEnergy uses bp:RatedEnergy and thus float and not double
* originalPowerCapability in aasx a Property, in BatteryPass a SML with SMC with the two properties: atSoC and powertCapabilityAt

* to be checked whether the units are identical to what is defined in ECLASS

## Information

* "ratedEnergy" was renamed to "CertifiedUsableBatteryEnergy"
* there is no semanticId for batteryCategory
* In BatteryPass TemperatureRangeIdleState was modelled as one property with a range constraint with min= -20 and max=60. Now there are two properties for it, TemperatureRangeIdleStateUpperBoundary and TemperatureRangeIdleStateLowerBoundary
* Length not existing in BatteryPass 
* Description of Length, Height, Width should be updated. Where is the Diameter mentioned in Length? Where is the depth mentioned in Width and Length.
* VoltagEntity: min and max should be switched
* semanticId "https://admin-shell.io/ZVEI/TechnicalData/FurtherInformation/1/1" should be reconsidered
* Capacity seems wrong: all need to be optional. Only for Pack it is mandatory. But not every battery is a Pack. Not all three properties are needed since a battery has exactly one batteryCategory. This is only because there are three different IRDIs for it. So either we have three SMT, one for each battery category or we need to do it in a generic way.
* InitialInternalResistance is different in BatteryPass. In BatteryPass it is a list of "ohmicResistance" and "batteryComponent" pairs with batteryComponent being cell, pack and module.
* in BatteryPass CurrentSelfDischargingRateValue is float, here InitialSelfDischargingRate is integer. Same for InitialRoundTripEnergyEfficiency, here integer, in BatteryPass for example RemainingRoundTripEnergyEfficiencyValue is float


### Open issues

* https://github.com/batterypass/BatteryPassDataModel/issues/33 Warrenty VS Warranty (Payload name already Warranty)

