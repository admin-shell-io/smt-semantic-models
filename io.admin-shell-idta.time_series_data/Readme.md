# Scope

This namespace is reserved for the Submodel Template Specification (SMT) IDTA-02008 Time Series Data

Namespace: urn:samm:io.admin-shell.idta.time_series_data


# General

The folder "gen" for each version contains sammple JSON files, the JSON schema and html generated for the aspect model(s)

# Copyright Information

This model is using the models of the BatteryPass Consortium: https://github.com/batterypass/BatteryPassDataModel
with license CC BY 4.0. (urn:samm:io.BatteryPass.Circularity:1.2.0#)


# Changelog
All notable changes to this model will be documented in this section.

## [1.1.0] - July 2026

based on IDTA-02008 Version 1.1.1 for V3.1

Deviations from aasx:

* add SML Records as parts of Metadata with cardinality 0..1, Record within with cardinality 0..*
* add SML ExternalSegments, InternalSegments and LinkedSegments with cardinality 0..1, Segment within with cardinality 0..*
* Change InternalSegments/Records from SMC to SML
* Change sampleAccelerationX, Y, Z to start with Capital Letter (to be consistent with Specification)
* Change xs:long to xs:dateTime for ExternalSegment/StartTime, /EndTime, /LastUpdate (to be consistent with Specification)
* Change xs:long to xs:dateTime for LinkedSegment/StartTime, /EndTime, /LastUpdate (to be consistent with Specification)
* Change xs:long to xs:dateTime forInternalSegment/StartTime, /EndTime, /LastUpdate (to be consistent with Specification)
* Record/Time has cardinality 1 instead of 1..*
* remove semanticId from Record/Time
* add administration/templateId

* question: Metadata/Records Record/Time has a qualifier AllowedIdShort with Time[\d{2,3}]
* question: cardinality Record/Time really 1..* or just 1 ?
* question: why has lastUpdate Type xs:string and not xs:time? ExternalSEgment/endTime startTime usw. Properyt Record/time has type xs:long...

* not possible to define two different types String or long as done for duration, in .aasx it is xs:string
* Record/Time can be UTc or Tai or relative: it is expected that the correct semanticId is provided by the data provider. Cannot be used like this in Value-Only serialization. 
No aasx file can be provided since nor "OR" semantics for supplementalSemanticIds.

* question: Record/Time might be modelled as SML with Properties, with Property has an enumeration "UtcTime", "TaiTime", "RelativePointInTime" and "RelativeTimeDuration". 
In the spec there is a {Variable} with the corresponding semanticId.

Spec:

* Typo in pdf: TIMESTSAMP
* Typo seamantic




