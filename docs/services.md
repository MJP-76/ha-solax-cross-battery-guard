# Services

The integration exposes two services for automations and manual control.

## `dual_battery_control.prevent_cross_charge`

Manually trigger cross-charge prevention.

- Supports a **dry-run mode** — report what would change without applying it.
- Use it to test a configuration or to force a correction outside the
  automatic schedule.

```yaml
service: dual_battery_control.prevent_cross_charge
data:
  dry_run: true
```

## `dual_battery_control.set_auto_correction`

Toggle automatic correction on or off.

- Equivalent to flipping the switch control entity exposed on the dashboard.

```yaml
service: dual_battery_control.set_auto_correction
data:
  enabled: true
```

## Dashboard control entities

These mirror the same controls in the UI so automations can read state:

- **Auto-correction** — switch (is the correction engine live?)
- **Check interval** — number (how often the rule engine runs)
- **Correction mode** — select (how aggressively to respond)

## WhatsApp notifications

When corrections are applied automatically, the integration sends a WhatsApp
message (via the `whatsapp.send_message` service, targeting the number
configured during setup) with the reason and the new amp limit per action —
letting you know the batteries were acting up and the fix applied.