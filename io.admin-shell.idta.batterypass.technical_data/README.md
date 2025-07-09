# Scope

This namespace is reserved for the Submodel Template Specification (SMT) [IDTA-020xx Technical Data for Batteries](https://industrialdigitaltwin.org/wp-content/uploads/2022/10/IDTA-02003-1-2_Submodel_TechnicalData.pdf)

Namespace: urn:samm:io.admin-shell.idta.batterypass.technical_data

# General

The folder "gen" for each version contains sammple JSON files generated for the aspect model(s)
The folder "input" contains source files like .aasx or the submodel template specification itself

# Changelog
All notable changes to this model will be documented in this section.

## [1.0.0] - add date

Contained Files:

* TechnicalData.ttl: the aspect model for the SMT : the _see_ attribute needs to be extended to include the ID of the concrete technical data SMT derived from this generic SMT

* furtherInformation_generic.ttl : this file needs to be substituted when deriving a concrete techncial data SMT from this generic SMT
* technicalProperties_generic.ttl : this file needs to be substituted when deriving a concrete techncial data SMT from this generic SMT
* generalInformation_shared.ttl : as defined in SMT IDTA-02003, probably to be substituted by the entity in generalInformation_nameplate_shared.ttl
* generalInformation_nameplate_shared.ttl  : this file is identical to generalInformation_shared but reused the corresponding properties form SMT Nameplate 3.0.0
* productImages_shared.ttl : property for a set of product images
* productClassifications_shared.ttl


Dependencies:

* urn:samm:io.admin-shell.idta.generic.technical_data:1.0.0# 
* urn:samm:io.admin-shell.idta.nameplate:3.0.0#   - if generalInformation_nameplate_shared.ttl is used
* urn:samm:io.admin-shell.idta.shared:3.1.0#


In the following only deviations are documented:

### Added



		
### Changed




### Removed



## Open Questions

### TO BE CLARIFIED: samm:see <https://admin-shell.io/ZVEI/TechnicalData/Submodel/1/2> ; since it seems to be V1.0?
### still open properties of Efficiency
### still open properties of Resistance
### still open properties of Capacity
### for consistency SMC for TemperatureRangeIdleStateBoundaries should be introduced

