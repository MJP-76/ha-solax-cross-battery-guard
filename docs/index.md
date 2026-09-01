# Dual Battery Control

[![Home Assistant][badge-home-assistant]][home-assistant]
[![HACS][badge-hacs]][hacs]
[![HACS Validation][badge-hacs-validation]][workflow-hacs-validation]
[![Hassfest][badge-hassfest]][workflow-hassfest]
[![CI][badge-ci]][workflow-ci]
[![Release][badge-release]][releases]
[![Built with AI][badge-built-with-ai]][built-with-ai]

A Home Assistant custom component for **monitoring and preventing
cross-charging** between batteries in dual-inverter setups.

It is configured through Home Assistant's UI config flow (not
`configuration.yaml`) and can create a Lovelace dashboard automatically from
the entities you choose, with separate battery blocks and live SOC/power trend
cards.

Current release: `0.3.3`. Default dashboard URL path: `dualbatterycontrol`.

## What this integration does

- Battery registry
- Rule engine (cross-charge, SOC divergence, thermal)
- Correction engine — automatic prevention of cross-charging
- Diagnostics and a repairs helper
- Config flow and options flow for selecting battery entities, dashboard, and
  correction settings
- WhatsApp notifications when cross-charge corrections are applied
- Enhanced correction history with amps, action type, and new limit per event
- Dashboard control entities (switch, number, select) for auto-correction,
  check interval, and correction mode
- Auto-calculated aggressiveness based on cross-charge severity
- Two services: `prevent_cross_charge` (manual trigger with dry-run mode) and
  `set_auto_correction` (toggle)

## Where to go next

| Topic | Page |
|---|---|
| Install and set up | [Installation](installation.md) |
| Why dual-inverter setups cross-charge | [Background](background.md) |
| Services you can call from automations | [Services](services.md) |
| The auto-created Lovelace dashboard | [Dashboard](dashboard.md) |

[badge-home-assistant]: https://img.shields.io/badge/Home%20Assistant-41BDF5?style=flat-square&logo=homeassistant&logoColor=white
[home-assistant]: https://www.home-assistant.io/
[badge-hacs]: https://img.shields.io/badge/HACS-Custom-41BDF5.svg
[hacs]: https://github.com/hacs/integration
[badge-hacs-validation]: https://img.shields.io/badge/HACS%20Validation-passing-brightgreen
[workflow-hacs-validation]: https://github.com/MJP-76/ha-dual-battery-control/actions/workflows/validate.yml
[badge-hassfest]: https://img.shields.io/github/actions/workflow/status/MJP-76/ha-dual-battery-control/hassfest.yml?branch=main&label=Hassfest
[workflow-hassfest]: https://github.com/MJP-76/ha-dual-battery-control/actions/workflows/hassfest.yml
[badge-ci]: https://github.com/MJP-76/ha-dual-battery-control/actions/workflows/ci.yml/badge.svg
[workflow-ci]: https://github.com/MJP-76/ha-dual-battery-control/actions/workflows/ci.yml
[badge-release]: https://img.shields.io/github/v/release/MJP-76/ha-dual-battery-control?style=flat&label=Release
[releases]: https://github.com/MJP-76/ha-dual-battery-control/releases
[badge-built-with-ai]: https://img.shields.io/badge/Built%20with-AI-black?logo=openai&logoColor=white
[built-with-ai]: https://openai.com