# Scope

This namespace is reserved for the Submodel Template Specification (SMT) IDTA-02006 Digital Nameplate

# Changelog
All notable changes to this model will be documented in this section.

## [4.0.0] - October 2026

alignment with IDTA-02006 V4.0

Major changes:
- new payload name for MarkingName, now TypeOfConformityRegulationCertification
- new payload name for IssueDate, now DateOfIssue
- new payload name for ExpiryData, now EndOfValidity
- new payload name for MarkingAdditionalText, now AdditionalMarkingText


Minor changes:

* add new samm:see attributes from IDTA-02006 V4.0

## [3.0.1] - October 2026

Other changes:

* editorial changes in preferred names and description for consistency only (usage of capital and small letters etc.)
* cleanup unused element
* newly generated files .html .json .schema-json
* update licence information if missing

## [3.0.0] - 2005-03-11

for changelog see Annex B in [IDTA-02006-3-0](https://industrialdigitaltwin.org/en/wp-content/uploads/sites/2/2024/11/IDTA-02006-3-0_Submodel_Digital-Nameplate.pdf)

Source GitHub IDTA for .aasx file and Submodel Template Specification etc.: https://github.com/admin-shell-io/submodel-templates/tree/main/published/Digital%20nameplate

Contained Files:

* Nameplate.ttl: the aspect model for the SMT
* AddressInformtion_shared.ttl: ContactInformation with properties defined as mandatory as per SMT IDTA-02006-3-0

Dependencies:

* urn:samm:io.admin-shell.idta.contact_information:3.0.0
* urn:samm:io.admin-shell.idta.shared:3.1.0


In the following only deviations from IDTA-02006-3-0 are documented:

### Added

* added preferred names. Attention: they are not yet aligned with the names as defined in the IEC CDD dictionary or ECLASS
* added some German descriptions and preferred names
		
### Changed

* descriptions changed conformant to [SAMM best practices](https://eclipse-esmf.github.io/samm-specification/snapshot/appendix/best-practices.html), i.e. start with captial letter and end with period.

### Removed

* SMT attribute _Nameplate/AssetSpecificProperties_ is not contained since it is generic: if needed the property can be added with defined SAMM properties as needed.