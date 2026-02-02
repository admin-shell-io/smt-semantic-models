# Scope

This namespace is reserved for the Submodel Template Specification (SMT) IDTA-02002-1-0 Contact Information

# Changelog
All notable changes to this model will be documented in this section.

## [1.0.0] - 2005-03-11

for changelog see Annex B in [IDTA-02002-1-0](https://industrialdigitaltwin.org/wp-content/uploads/2022/10/IDTA-02002-1-0_Submodel_ContactInformation.pdf)


Source GitHub IDTA for .aasx file and Submodel Template Specification etc.: https://github.com/admin-shell-io/submodel-templates/tree/main/published/Contact%20Information 

Contained Files:

* ContactInformations.ttl: the aspect model for the SMT, mainly needed for example JSON payload etc., Contact Information typically is just shared and not a stand-alone aspect
* ContactInformation_shared.ttl: shared aspect elements
* ContactInformation_enum_shared.ttl: shared enumeration and values

Dependencies:

* urn:samm:io.admin-shell.idta.shared:3.1.0


In the following only deviations from IDTA-02006-3-0 are documented:

### Added

* new property "postalCode" because zipCode only allows numbers´- Attention: namespace version was not changed (see https://github.com/admin-shell-io/submodel-templates/issues/215)
* added preferred names. Attention: they are not yet aligned with the names as defined in the IEC CDD dictionary or ECLASS
* added some German descriptions and preferred names
* added missing example values
		
### Changed

* ContactInformation/Language needs to be a SML, i.e. modelled as Set
* ContactInformation/IPCommunication needs to be a SML, i.e. modelled as Set
* If same attribute occurred in different elements a suffix was added to the property name (the payload name remains). 
  Example: ContactInformation/AddressOfAdditionalLink and IPCommunication/AddressOfAdditionalLink, therefore SAMM propoerty name for IPCommunciation is addressOfAdditionalLinkOfIpCommunicationChannel. 
* descriptions changed conformant to [SAMM best practices](https://eclipse-esmf.github.io/samm-specification/snapshot/appendix/best-practices.html), i.e. start with captial letter and end with period. No usage of AAS specific terms like SMC.
* example values for properties roleOfContactPerson, typeOfTelphone, typeOfEmailAddress and typeOfFaxNumber are no IRDIs as recommended by IDTA-02006-3-0 but the value of the enumeration value

### Removed

--