# Installation

## HACS (recommended)

1. In HACS, add this repository as a custom repository (category: **Integration**):
   `https://github.com/MJP-76/ha-dual-battery-control`
2. Search for "Dual Battery Control" in HACS and install it.
3. Restart Home Assistant.

## Manual

1. Copy `custom_components/dual_battery_control/` into your Home Assistant
   `config/custom_components/` directory.
2. Restart Home Assistant.

## First-time setup

1. Go to **Settings → Devices & Services → Add Integration** and search for
   "Dual Battery Control".
2. Select the **battery entities** (SOC/power sensors) for both batteries.
3. Choose whether the integration should **create a dashboard** and which
   settings to enable.
4. Decide whether **auto-correction** should be on and how aggressive it
   should be.

The options flow lets you change battery entities, the dashboard setup, and
correction settings afterwards. Wall-clock corrections are applied
automatically while auto-correction is enabled — see [Services](services.md)
for the manual trigger and its dry-run mode.

!!! note "Correct the battery identities carefully"

    Getting the two batteries swapped means the correction engine will act on
    the wrong inverter, so double-check which entity belongs to which battery
    during setup.