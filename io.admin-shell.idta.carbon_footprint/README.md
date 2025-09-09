# Scope

This namespace is reserved for the Submodel Template Specification (SMT) IDTA-02023 Version 1.0 Carbon Footprint

Previous Version: 0.9

Source GitHub: https://github.com/admin-shell-io/submodel-templates/tree/main/published/Carbon%20Footprint/1/0
Source Content Hub of the IDTA: [IDTA-02023 V1.0](https://industrialdigitaltwin.org/en/wp-content/uploads/sites/2/2025/03/IDTA-02023_Submodel_CarbonFootprint.pdf)

# How to add product or sector specific Carbon Footprints

* create new folder for namespace with name io.admin-shell.idta.carbon_footprint.<your pcf, e.g. PACT>
* create file <your pcf>_shared.ttl and define the samm:Entity for your pcf
* adapt CarbonFootprint.ttl
** copy file CarbonFootprint.ttl to the folder and rename it to CarbonFootprint<your pcf>.ttl
** substitute "@prefix : <urn:samm:io.admin-shell.idta.carbon_footprint:1.0.0#>"  with your new namespace, e.g. "@prefix : <urn:samm:io.admin-shell.idta.carbon_footprint.pact:1.0.0#>"
*  adapt pcfInformation_generic.ttl
** copy ProductOrSectorSpecificCarbonFootprints_generic.ttl to folder and rename it to ProductOrSectorSpecificCarbonFootprints_shared.ttl
** substitute "samm:dataType  :ProductOrSectorSpecificPcfInformationEntity" with the new data type you defined in <your pcf>_shared.ttl. Remove :ProductOrSectorSpecificPcfInformationEntity


# Changelog
All notable changes to this model will be documented in this section.

## [1.0.0] - <add date>

for changelog see  [IDTA-02023 V1.0, section "Version history"](https://industrialdigitaltwin.org/en/wp-content/uploads/sites/2/2025/03/IDTA-02023_Submodel_CarbonFootprint.pdf)

Contained Files:

* CarbonFootprint.ttl
* pcfInformation_generic.ttl


Dependencies:

* 

# Deviations:
- preferred names in English typically starting with small letter
- description starting with capital letter and ending with "."
- if description contains AAS specific wording like "Submodel" etc. this is omitted
- In Contact Information Street is defined as street names and house number, in Pcf there are two separate properties. Neverthelesse the street property from Contact Information was used. In Contact Information it has IRDI urn:irdi:0173-1#02-AAO128#002. In Pcf it has IRDI 0173-1#02-ABH956#003.
- SAMM does not allows numbers in names, therefore pcfCo2eq was renamed to pcfCoEq
- Property "ArbitraryContent" as part of "PcfInformation" is modelled an SAMM Entity without properties
- enumerations are not (yet) modelled

# Known Issues generation of aasx from aspect model:
- SubmodelElement File is realized as SMC with two properties (ExplanatoryStatement and PcfRuleOnlineReference)
- no template qualifiers generated
- the idShort of the Element within a SML has the idShort of the list, not of the element
- SMC ExternalPcfApi not generated with its properties, properties are missing
- SMC ProductOrSectorSpecificRule not generated with its properties, properties are missing