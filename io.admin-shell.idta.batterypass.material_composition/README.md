# Scope

This namespace is reserved for the Submodel Template Specification (SMT) IDTA-02035-6 Digital Battery Passport - Part 6: Material Compostion

Namespace: urn:samm:io.admin-shell.idta.batterypass.material_composition

The battery passport consists of the following 7 parts:

*	Digital Battery Passport - Part 1: Digital Nameplate (IDTA-02035-1)
*	Digital Battery Passport - Part 2: Handover Documentation (IDTA-02035-2)
*	Digital Battery Passport - Part 3: Product Carbon Footprint  (IDTA-02035-3)
*	Digital Battery Passport - Part 4: Technical Data (IDTA-02035-4) 
*	Digital Battery Passport - Part 5: Product Condition  (IDTA-02035-5)
*	Digital Battery Passport - Part 6: Material Composition  (IDTA-02035-6)
*	Digital Battery Passport - Part 7: Circularity  (IDTA-02035-7)

This model is using the models of the BatteryPass Consortium: https://github.com/batterypass/BatteryPassDataModel/tree/main/BatteryPass/io.BatteryPass.MaterialComposition (urn:samm:io.BatteryPass.MaterialComposition:1.2.0)
with license CC BY-NC 4.0.

Source GitHub IDTA for .aasx file and Submodel Template Specification etc.: https://github.com/admin-shell-io/submodel-templates 


# General

The folder "gen" for each version contains sammple JSON files, the JSON schema and html generated for the aspect model(s)

# Changelog
All notable changes to this model will be documented in this section.

## [1.0.2] - October 2026

Major changes:

* conformant to DIN SPEC 99100:2025 not only CAS but also IUPAC is allowed for material identification or naming. ([#140](https://github.com/admin-shell-io/smt-semantic-models/issues/140))
* make harzardousSubstanceImpact and hazardousSubstanceConcentration mandatory  ([#113](https://github.com/admin-shell-io/smt-semantic-models/issues/113))
* materialComposition batteryPassport: fix descriptions not being consistent with intention  ([#124](https://github.com/admin-shell-io/smt-semantic-models/issues/124))
* batteryMaterials and hazardousSubstances: change threshold of 0.1 % weight by weight to 1% conformant to DIN DKE SPEC 99100  ([#54](https://github.com/admin-shell-io/smt-semantic-models/issues/154))

Other changes:


* add date to DIN DKE references in descriptions: DIN DKE Spec 99100:2025-02 ([#117](https://github.com/admin-shell-io/smt-semantic-models/issues/117))
* editorial changes in preferred names and description for consistency only (usage of capital and small letters etc.)
* cleanup unused element
* newly generated files .html .json .schema-json
* update licence information if missing

## [1.0.1] - April 2026

Major changes:

* change: measurement unit of BatteryMaterialMass from gram to kilogram (https://github.com/admin-shell-io/smt-semantic-models/issues/85[#85])
* change: make :batteryMaterialMass optional (https://github.com/admin-shell-io/smt-semantic-models/issues/83[#83])
* change: make :hazardousSubstanceClass, :hazardousSubstanceClass, :hazardousSubstanceConcentration, :hazardousSubstanceImpact and :hazardousSubstanceLocation optional in :HazardousSubstance (https://github.com/admin-shell-io/smt-semantic-models/issues/83[#83])


Minor changes (not affecting payload or specification):

* fix namespace in Namespace.ttl
* rename HubstanceSubstanceLocationEntity to HazardousSubstanceLocation
* rename :BatteryLocation to BatteryComponentEntity
* editorial changes in descriptions
* example values added for several properties. Note: Since SAMM does not allow example values for lists the example value "May cause an allergic skin reaction" for Impact in HarzadousSubstanceImpact was added directly in .aasx
* split file  MaterialComposition_shared.ttl into MaterialComposition_shared.ttl and enum_HazardousSubstanceClass_shared.ttl


Contained Files:

* MaterialComposition.ttl
* MaterialComposition_shared.ttl
* enum_HazardousSubstanceClass_shared.ttl
* Namespace.ttl


## [1.0.0] - February 2026

for changelog see  [IDTA-02035-6 V1.0, section "Version history"]()

Contained Files:

* MaterialComposition.ttl
* MaterialComposition_shared.ttl
* Namespace.ttl







