# Scope

This namespace is reserved for the Submodel Template Specification (SMT) IDTA-02035-1 Digital Battery Passport - Part 1: Digital Nameplate


Namespace: urn:samm:io.admin-shell.idta.batterypass.digital_nameplate

This SMT is derived from IDTA-02006 Digital Nameplate V3.0

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

The folder "gen" for each version contains sammple JSON files, the JSON schema and html generated for the aspect model(s)

# Changelog
All notable changes to this model will be documented in this section.

## [1.0.0] - 2025-12

Contained Files:

* Nameplate.ttl: the aspect model for the SMT
* BatteryStatus_enum.ttl: enumeration of :batteryStatus
* AddressInformation_shared.ttl: copy of :addressInformation of urn:samm:io.admin-shell.idta.batterypass.digital_nameplate:1.0.0#addressInformation but with updated description to include reference to DIN DKE SPEC 99100

# Dependencies:

* urn:samm:io.admin-shell.idta.digital_nameplate:3.0.0
* urn:samm:io.admin-shell.idta.contact_information:3.0.0
* urn:samm:io.admin-shell.idta.shared:3.1.0
* urn:samm:io.BatteryPass.GeneralProductInformation:1.2.0

# Deviations from urn:samm:io.admin-shell.idta.digital_nameplate:3.0.0

The following optional attributes are mandatory:

* serialNumber is mandatory
* dateOfManufacture is mandatory
* uniqueFacilityIdentifier is mandatory
* markings are mandatory

The following mandatory attributes are not included:

* manufacturerProductDesignation
* orderCodeOfManufacturer

The followign optional attributes are not included:

* manufacturerProductDesignation
* manufacturerProductRoot
* manufacturerProductFamily
* manufacturerProductType
* productArticleNumberOfManufacturer
* yearOfConstruction
* HardwareVersion
* FirmwareVersion
* SoftwareVersion
* countryOfOrigin
* companyLogo
* assetSpecificProperties


The following attributes are new:

* operatorIdentifier
* manufacturerIdentifier
* euDeclarationOfConformity
* resultsOfTestReportsProvingCompliance
* dateOfPuttingIntoService

# Overall Deviations

see IDTA-02006

