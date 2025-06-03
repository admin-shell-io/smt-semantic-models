# Scope

This namespace is reserved for the Submodel Template Specification (SMT) IDTA-02023 Version x.y (1.0 is the old one)  Carbon Footprint

# Changelog
All notable changes to this model will be documented in this section.

## [1.0.0] - <add date>

for changelog see  [IDTA-02023](https://industrialdigitaltwin.org/en/content-hub/submodels)

Contained Files:

* pcf.ttl

Dependencies:

* 

Deviations:

- ProductCarbonFootprint modelled as SML, i.e. property with payload name "ProductCarbonFootprints"
- PcfCalculationMethod within ProductCarbonFootprint and within ProductOrSectorSpecificCarbonFootprint modelled as SML, i.e. property with payload name "PcfCalculationMethods"
- productOrSectorSpecificRules  within ProductOrSectorSpecificCarbonFootprint modelled as SML, i.e. property with payload name "ProductOrSectorSpecificRules"
- Contact Information reused from Contact Information SMT  - to be checked. Some optional fields are mandatory
- PcfCalculationMethod within ProductCarbonFootprint modelled as 1 and not 1..*: if there are several PCF then several ProductCarbonFootprint objects will be created
- In Contact Information Street is defined as street names and house number, in Pcf there are two separate properties. Neverthelesse the street property from Contact Information was used. In Contact Information it has IRDI urn:irdi:0173-1#02-AAO128#002. In Pcf it has IRDI 0173-1#02-ABH956#003.
- PcfInformation within ProductOrSectorSpecificCarbonFootprint is no Set, it is an Entity (SMC)
- SAMM does not allows numbers in names, therefore pcfCo2eq was renamed to pcfCoEq
