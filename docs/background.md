# Background

This component was created to solve **cross-charging** between two batteries
connected to a pair of **SolaX SKU-5000E inverters** that do not support
Master/Slave co-ordination.

In such setups, each inverter independently decides when to charge or
discharge its battery. That can lead to one battery discharging into the
other — wasting energy and reducing efficiency.

Dual Battery Control detects this condition and can automatically adjust
charge-current limits to break the loop.

## How the rules work

The integration runs a rule engine that watches for problem conditions:

| Rule | What it guards against |
|---|---|
| **Cross-charge** | One battery discharging into the other. |
| **SOC divergence** | Batteries drifting far apart in state of charge. |
| **Thermal** | Temperature conditions that would make aggressive charging unsafe. |

When a rule fires, the correction engine reacts — by default automatically —
with an action that depends on the configured **correction mode** and
**aggressiveness** (auto-calculated from cross-charge severity). Every applied
correction is recorded with the amps, action type, and new limit per event, so
you get an audit trail of what the integration did and why.