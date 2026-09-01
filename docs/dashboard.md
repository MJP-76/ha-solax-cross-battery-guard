# Dashboard

The integration can create a Lovelace dashboard automatically from the
entities you choose during setup.

- **Separate battery blocks** — one per battery, with its SOC, power, and
  status.
- **Live SOC/power trend cards** — so you can watch the two batteries against
  each other and see the correction engine at work.
- **Default URL path:** `dualbatterycontrol`.
- **Control entities** — the auto-correction switch, check interval, and
  correction mode select are surfaced here.

## Reset the dashboard

If the dashboard ever gets out of step (for example after an update), you can
recreate it via the integration's **Configure** options. Dashboard
customisations you have made yourself are preserved across reloads and
updates.