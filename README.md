# Home Assistant PV Module Monitoring Dashboard

Advanced photovoltaic module monitoring for **Home Assistant** with per-module visualization, heatmaps, diagnostics, and performance analysis.

Designed for **Huawei optimizers / module-level telemetry**, but adaptable to other systems.

## Features

### Module Dashboard
- Real physical module layout
- Per-module values:
  - Power (W)
  - Voltage (V)
  - Temperature (°C)
  - Total energy (kWh)
- Status indicator (normal / warning / alarm)

### Heatmap View
Visual performance overview of the array.

Color coding based on **absolute deviation from row average**:

| Color | Meaning |
|---|---|
| Blue | Normal operation |
| Orange | More than 15 W below row average |
| Red | More than 30 W below row average |

Additional indicators:
- ⚠ Temperature delta warning
- 🔥 High temperature delta

### PV Diagnostics
Provides deeper system insight:
- Solar radiation reference
- Expected module power
- Row average performance
- Temperature delta analysis
- Weakest module detection

### PV Pro Monitoring
Advanced analytics including:
- Row mismatch calculation
- Absolute module deviation
- Hottest module detection
- System performance evaluation
- Simple diagnostic status text

## Example Metrics

The system calculates:
- Module performance vs. expected output
- Row average power
- Row mismatch percentage
- Temperature deltas between modules
- Absolute power deviation (W)

These values help detect:
- shading
- dirty modules
- optimizer issues
- module degradation
- thermal anomalies

## Installation

1. Copy the YAML packages into your Home Assistant `packages` directory.

Example path:

```text
/config/packages/
```

Files:
- `pv_super_allinone_package.yaml`
- `pv_pro_addon_package.yaml`

2. Restart Home Assistant.

3. Import the dashboards using **Raw YAML mode**.

Suggested dashboards:
- `pv_module`
- `pv_heatmap`
- `pv_diagnose`
- `pv_pro`

## Requirements

Home Assistant with the following custom cards installed via **HACS**:
- `button-card`
- `layout-card`

Optional:
- `mushroom`

## Tested With
- Huawei inverter + Huawei optimizers
- Ecowitt solar radiation sensor
- Home Assistant 2025+

## Notes

Efficiency values above 100% may occur if:
- the solar radiation sensor measures **horizontal irradiance**
- the PV modules are **tilted**

This is normal and expected.

## License

MIT License

## Screenshots

Add screenshots of your dashboards here:
- Module layout
- Heatmap view
- Diagnostic dashboard
- PV Pro analytics
