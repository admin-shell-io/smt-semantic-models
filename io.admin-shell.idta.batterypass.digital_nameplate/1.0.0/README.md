# BatteryNameplate SAMM 2.2.0 role based models

This PoC models role based differences via `samm:AbstractEntity` and `samm:extends`.

## Structure

- `BatteryNameplate_common.ttl`
  - shared Property/Characteristic definitions
  - `BatteryNameplateBaseEntity` (`samm:AbstractEntity`)
  - contains only properties whose cardinality is identical for all roles
- `BatteryNameplate_BatterySupplier.ttl`
  - `BatteryNameplateSupplierEntity` extends the base entity
  - AddressInformation, DateOfPuttingIntoService, OperatorIdentifier and ManufacturerIdentifier are optional
- `BatteryNameplate_EconomicOperator.ttl`
  - `BatteryNameplateEconomicOperatorEntity` extends the base entity
  - the same four properties are mandatory

## Aspect wrapper and payload shape

SAMM does not support Aspect-to-Aspect inheritance. Each Aspect therefore exposes one root Property whose Characteristic is a `samm-c:SingleEntity` pointing to the corresponding concrete Entity.

This means the JSON payload has one additional object level compared with a flat Aspect whose properties are all declared directly at Aspect root level.

Example supplier payload shape:

```json
{
  "batteryNameplateSupplier": {
    "URIOfTheProduct": "...",
    "ManufacturerName": { "en": "Example Corp" },
    "SerialNumber": "..."
  }
}
```
