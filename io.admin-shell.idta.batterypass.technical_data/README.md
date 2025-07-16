# Scope

This namespace is reserved for the Submodel Template Specification (SMT) [IDTA-020xx Technical Data for Batteries](https://industrialdigitaltwin.org/wp-content/uploads/2022/10/IDTA-02003-1-2_Submodel_TechnicalData.pdf)

This SMT is derived from IDTA-02003-1-2 Generic Technical Data 1.2 

Namespace: urn:samm:io.admin-shell.idta.batterypass.technical_data

# General

The folder "gen" for each version contains sample JSON files generated for the aspect model(s)


# Changelog
All notable changes to this model will be documented in this section.

## [1.0.0] - add date

Contained Files:

* TechnicalData.ttl: the aspect model for the SMT 
* technicalProperties_shared.ttl




Dependencies:

* urn:samm:io.admin-shell.idta.generic.technical_data:1.2.0# 
* urn:samm:io.admin-shell.idta.nameplate:3.0.0#  
* urn:samm:io.admin-shell.idta.shared:3.1.0#


In the following only deviations are documented:

### Added



		
### Changed




### Removed


## Deviations

* IRDIs from ECLASS not added in case properties of BatteryPass were reused
* Some descriptions deviate from those in the specification in case properties of BatteryPass were reused
* example values not added in case properties of BatteryPass were reused
* added: missing description for Capacity
* added: same description for Height as for Width.
* for nominalVoltage, MaxVoltage and MinVoltage the descriptions of BatteryPass were taken
* in BatteryPass PowerCapabilityat20Charge or 80Charge is float and not double
* in BatteryPass originalPowerCapabilityLimits is not existing but PowerCapabilities is float, Characteristic bp:PowerCapabilityAtSoc is used
* ratedEnergy from BatteryPass was used as Characteristic for MaximumAllowedBatteryEnergy, but is float, in .docs it is double
* maximumPermittedBatteryPower and originalPowerCapabilityLimits uses bp:PowerCapabilityAtSoc and thus is float and not double
* maximumAllowedBatteryEnergy uses bp:RatedEnergy and thus float and not double

* to be checked whether the units are identical to what is defined in ECLASS

## Information

* "ratedEnergy" was renamed to "CertifiedUsableBatteryEnergy"
* there is no semanticId for batteryCategory
* In BatteryPass TemperatureRangeIdleState was modelled as one property with a range constraint with min= -20 and max=60. Now there are two properties for it
* Length not existing in BatteryPass 
* Description of Length, Height, Width should be updated. Where is the Diameter mentioned in Length? Where is the depth mentioned in Width and Length.
* VoltagEntity: min and max should be switched
* semanticId "https://admin-shell.io/ZVEI/TechnicalData/FurtherInformation/1/1" should be reconsidered
* Capacity seems wrong: all need to be optional. Only for Pack it is mandatory. But not every battery is a Pack. Not all three properties are needed since a battery has exactly one batteryCategory. This is only because there are three different IRDIs for it. So either we have three SMT, one for each battery category or we need to do it in a generic way.
* InitialInternalResistance is different in BatteryPass. In BatteryPass it is a list of "ohmicResistance" and "batteryComponent" pairs with batteryComponent being cell, pack and module.
* in BatteryPass CurrentSelfDischargingRateValue is float, here InitialSelfDischargingRate is integer. Same for InitialRoundTripEnergyEfficiency, here integer, in BatteryPass for example RemainingRoundTripEnergyEfficiencyValue is float


## Open Questions

### still open properties of Efficiency
### still open properties of Resistance
### for consistency SMC for TemperatureRangeIdleStateBoundaries should be introduced
### should be remove optional [ samm:property tech:productClassifications; samm:optional true ] from generic Technical Data? We should if we do not have a recommendation what to add there

