# Base Configs

## rack-environment-monitoring.yaml

```yaml
substitutions:
  # These variables are passed into the remote GitHub package
  device_name: "yourdevicename"
  device_friendly_name: "YOUR DEVICE NAME"

  # =================================================================
  # CCS811 CALIBRATION PHASES
  # =================================================================
  # PHASE 1 (Burn-In): Leave this exactly as an empty string ("") for the first week!
  # This makes the line disappear in the base config, allowing the sensor to settle.
  # 
  # PHASE 2 (Calibrated): Once you find the true floor in the logs, change it to:
  # ccs811_baseline_config: "baseline: 0xF0B9"
  # =================================================================
  ccs811_baseline_config: ""

packages:
  remote_base:
    # URL to your GitHub repository
    url: https://github.com/GdeBrienz/esphome_projects
    # The branch (e.g., main) or release tag (e.g., v1.0.0)
    ref: main 
    # The specific file to pull from that repository
    files: [rack-monitoring/rack-environment-monitoring.yaml]
    # How often ESPHome should check GitHub for changes
    refresh: 1d

# Enable Home Assistant API
api:
  encryption:
    key: "YOURENCRYPTIONKEY_CHANGEIT"

ota:
  - platform: esphome
    password: "YOUROTAKEY_CHANGEIT"
```
