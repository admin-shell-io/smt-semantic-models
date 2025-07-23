# Scope

This namespace is reserved for the Submodel Template Specification (SMT)  IDTA-02035-5 Digital Battery Passport - Part 5: Product Condition 

Namespace: urn:samm:io.admin-shell.idta.batterypass.product_condition

The battery passport consists of the following 7 parts:

*	Digital Battery Passport - Part 1: Digital Nameplate (IDTA-02035-1)
*	Digital Battery Passport - Part 2: Handover Documentation (IDTA-02035-2)
*	Digital Battery Passport - Part 3: Product Carbon Footprint  (IDTA-02035-3)
*	Digital Battery Passport - Part 4: Technical Data (IDTA-02035-4) 
*	Digital Battery Passport - Part 5: Product Condition  (IDTA-02035-5)
*	Digital Battery Passport - Part 6: Material Compostion  (IDTA-02035-6)
*	Digital Battery Passport - Part 7: Circularity  (IDTA-02035-7)

This model is using parts of the models relevant for dynamic data of the BatteryPass Consortium: https://github.com/batterypass/BatteryPassDataModel/tree/main/BatteryPass/io.BatteryPass.Performance
with license CC BY-NC 4.0.

Source GitHub IDTA: https://github.com/admin-shell-io/submodel-templates 
Source Content Hub of the IDTA: [IDTA-02035-5 V1.2]()

# Changelog
All notable changes to this model will be documented in this section.

## [1.2.0] - <add date>

for changelog see  [IDTA-02035-5 V1.2, section "Version history"]()

Contained Files:

* ProductCondition.ttl



Dependencies:

* urn:samm:io.BatteryPass.Performance:1.2.0

Deviations:
* informationOnAccidents is modelled as a DocumentSet (reuse from SMT HandoverDocumentation), in DIN SPEC 99100 it is described as a Reference to a pdf File.  