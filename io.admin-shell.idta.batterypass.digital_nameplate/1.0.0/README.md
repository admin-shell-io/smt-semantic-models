# BatteryNameplate SAMM 2.2.0 role based models

This PoC models role based differences via `samm:AbstractEntity` and `samm:extends`.

The roles and their obligations are taken from CX-0160-2 (Supplier Data Management), Appendix A "Data Submission Obligations based on Role in the Value Chain":

- **Battery Manufacturer**: column "Base Model Obligation"
- **Cell Producer**: column "Cell Producer to Batteries Obligation"

| Field | Battery Manufacturer | Cell Producer | Declared in |
| --- | --- | --- | --- |
| URIOfTheProduct | mandatory | mandatory | base entity |
| ManufacturerName | mandatory | mandatory | base entity |
| ManufacturerIdentifier | mandatory | mandatory | base entity |
| EUDeclarationOfConformity | mandatory | mandatory | base entity |
| DateOfPuttingIntoService | optional | optional | base entity |
| OperatorIdentifier | optional | optional | base entity |
| SerialNumber | mandatory | optional | role entity |
| DateOfManufacture | mandatory | optional | role entity |
| LifeCycleStage | mandatory | optional | role entity |
| UniqueFacilityIdentifier | mandatory | optional | role entity |
| AddressInformation | mandatory | optional | role entity |
| Markings | mandatory | optional | role entity |
| ResultsOfTestReportsProvingCompliance | mandatory | optional | role entity |

## Structure

- `BatteryNameplate.ttl`
  - shared Property/Characteristic definitions
  - `BatteryNameplateBaseEntity` (`samm:AbstractEntity`)
  - contains only properties whose obligation is identical for all roles
- `BatteryNameplate_BatteryManufacturer.ttl`
  - `BatteryNameplateBatteryManufacturerEntity` extends the base entity
  - the seven role-dependent properties are mandatory
- `BatteryNameplate_CellProducer.ttl`
  - `BatteryNameplateCellProducerEntity` extends the base entity
  - the same seven properties are optional

Role-dependent properties cannot be declared in the base entity, because `samm:optional` is inherited and cannot be overridden in a child entity.

## Aspect wrapper and payload shape

SAMM does not support Aspect-to-Aspect inheritance. Each Aspect therefore exposes one root Property whose Characteristic is a `samm-c:SingleEntity` pointing to the corresponding concrete Entity.

This means the JSON payload has one additional object level compared with a flat Aspect whose properties are all declared directly at Aspect root level.

Example cell producer payload shape:

```json
{
  "batteryNameplateCellProducer": {
    "URIOfTheProduct": "...",
    "ManufacturerName": { "en": "Example Corp" },
    "SerialNumber": "..."
  }
}
```
