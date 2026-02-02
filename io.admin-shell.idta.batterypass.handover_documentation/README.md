# Scope

This namespace is reserved for the Submodel Template Specification (SMT) IDTA-02035-2 Digital Battery Passport - Part 2: Handover Documentation

Namespace: urn:samm:io.admin-shell.idta.batterypass.handover_documentation

This SMT is derived from IDTA-02004 Handover Documentation

The battery passport consists of the following 7 parts:

*	Digital Battery Passport - Part 1: Digital Nameplate (IDTA-02035-1)
*	Digital Battery Passport - Part 2: Handover Documentation (IDTA-02035-2)
*	Digital Battery Passport - Part 3: Product Carbon Footprint  (IDTA-02035-3)
*	Digital Battery Passport - Part 4: Technical Data (IDTA-02035-4) 
*	Digital Battery Passport - Part 5: Product Condition  (IDTA-02035-5)
*	Digital Battery Passport - Part 6: Material Composition  (IDTA-02035-6)
*	Digital Battery Passport - Part 7: Circularity  (IDTA-02035-7)

Source GitHub IDTA for .aasx file and Submodel Template Specification etc.: https://github.com/admin-shell-io/submodel-templates 

# General

The folder "gen" for each version contains sammple JSON files, the JSON schema and html generated for the aspect model(s)

# Changelog
All notable changes to this model will be documented in this section.

## [2.0.0] - December 2025

for detailled changelog see [IDTA-02035-2](https://industrialdigitaltwin.org/en/content-hub/submodels)



Contained Files:

* HandoverDocumentation.ttl: the aspect model for the SMT


Dependencies:

* urn:samm:io.admin-shell.idta.handover_documentation
* urn:samm:io.admin-shell.idta.shared


In the following only deviations from IDTA-02035-2 are documented:



- mandatory properties not included:

  * from DocumentVersion:
  
	  * :keywords
	  * :statusSetDate
	  * :statusValue;
	  * :organizationName
	  * :organizationOfficialName

- mandatory properties made optional:

  * from DocumentVersion:
  
  	  * :version
	  * :description
	  
- optional properties not included:

  * :entities
  * :documentedEntities in :DocumentEntity
  * from DocumentVersion:

	  * :refersToEntities
	  * :basedOnReferences
	  * :translationOfEntities
	  * :previewFile

For further potential deviations see Aspect Model of IDTA-02004 