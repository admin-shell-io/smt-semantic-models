# Scope

This namespace is reserved for the Submodel Template Specification (SMT) IDTA-02099-1 Digital Product Passport - Part 1: Meta Data

Namespace: urn:samm:io.admin-shell.idta.dpp

So far the Digital Product Passport consists of the following parts:

*	IDTA-02099-1 Digital Product Passport - Part 1: Meta Data with namespace Namespace: urn:samm:io.admin-shell.idta.dpp.dpp_metadata


Source GitHub IDTA for .aasx file and Submodel Template Specification etc.: https://github.com/admin-shell-io/submodel-templates 


# General

The folder "gen" for each version contains sammple JSON files, the JSON schema and html generated for the aspect model(s)

# Changelog
All notable changes to this model will be documented in this section.

## [2.0.0] - November 2026

Target:

* align with JSON Schema https://repository.product-passport.ec.europa.eu/core/1.0.0/schemas/core.schema.json and  Semantic Data Artifacts of the EU Registry - DPP Registry (30.10.2026, V1.0)

Changes based on this alignment:

* elements "dppSchemaVersion", "economicOperatorId" and "facilityId" are not part of EU Semantic Data Artifacts: removed
* element "contentSpecificationIds" is now mandatory (in deviation to EN 18223:2026)
* enumeration values for "dppStatus" are now available (ValidStatus and InvalidStatus)
* enumeration values for "granularity" are using the complete path like "https://repository.product-passport.ec.europa.eu/core/vocabs/granularity-level#model" and not just "model"
* samm:see attributes added to properties for EC Vocabulary and http://data.europa.eu/eli/reg_impl/2026/1778/oj
* samm:descriptions and samm:preferredNames are adapted for properties
* in samm:descriptions added: "SOURCE" and "REFERENCES" information aligned with EC Vocabulary

Deviations from EC Vocabulary or JSON Schemas:

* samm:peferredNames consistent starting with small letters, in EC starting with capital letters
* sometimes samm:descriptions enhanced with additional information
* Note: in EC JSON Schema just a regular expression is used for enumeration dppStatus and granularity, here the values itself are modelled


## [1.0.1] - October 2026

Other changes:

* editorial changes in preferred names and description for consistency only (usage of capital and small letters etc.)
* cleanup unused element
* newly generated files .html .json .schema-json
* update licence information if missing

## [1.0.0] - May 2026

for changelog see  [IDTA-02099-1 V1.0, section "Version history"]()

Contained Files:

* DppMetadata.ttl


Dependencies:

None