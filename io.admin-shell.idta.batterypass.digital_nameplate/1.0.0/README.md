# BatteryNameplate SAMM 2.2.0 use-case models

## Files

- `BatteryNameplate.ttl`: shared SAMM Property and Characteristic definitions.
- `BatteryNameplate_BatterySupplier.ttl`: SAMM Aspect for the battery supplier use case.
- `BatteryNameplate_EconomicOperator.ttl`: SAMM Aspect for the economic operator use case.

## Use-case cardinalities

| Property | Battery Supplier | Economic Operator |
|---|---|---|
| AddressInformation | optional | mandatory |
| DateOfPuttingIntoService | optional | mandatory |
| OperatorIdentifier | optional | mandatory |
| ManufacturerIdentifier | optional | mandatory |

All other properties retain the mandatory/optional behavior of the provided BatteryNameplate model.