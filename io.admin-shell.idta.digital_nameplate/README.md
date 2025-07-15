# Scope

This namespace is reserved for the Submodel Template Specification (SMT) IDTA-02006 Digital Nameplate

# Changelog
All notable changes to this model will be documented in this section.

## [3.0.0] - 2005-03-11

for changelog see Annex B in [IDTA-02006-3-0](https://industrialdigitaltwin.org/en/wp-content/uploads/sites/2/2024/11/IDTA-02006-3-0_Submodel_Digital-Nameplate.pdf)

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