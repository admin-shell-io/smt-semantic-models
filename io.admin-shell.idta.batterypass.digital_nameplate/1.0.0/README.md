# BatteryNameplate SAMM 2.2.0 role based models

## Files

- `BatteryNameplate.ttl`: shared SAMM Property and Characteristic definitions.
- `BatteryNameplate_BatterySupplier.ttl`: SAMM Aspect for role battery supplier.
- `BatteryNameplate_EconomicOperator.ttl`: SAMM Aspect for role economic operator.

## Role based cardinalities

| Property | Battery Supplier | Economic Operator |
|---|---|---|
| AddressInformation | optional | mandatory |
| DateOfPuttingIntoService | optional | mandatory |
| OperatorIdentifier | optional | mandatory |
| ManufacturerIdentifier | optional | mandatory |

All other properties retain the mandatory/optional behavior of the provided BatteryNameplate model.
