# ESPHome Projects - Einwohnergemeinde Brienz

This repository contains the ESPHome configuration files used by the **Einwohnergemeinde Brienz** for various IoT and automation projects.

## 📌 Projects

### 📟 Rack Monitoring
Located in: [`/rack-monitoring`](./rack-monitoring)

A environmental monitoring system designed for server racks.
- **Hardware:** Olimex ESP32-PoE-ISO
- **Sensors:** MOD-ENV (BME280 for Temp/Hum/Press, CCS811 for eCO2/TVOC)
- **Features:** 
  - Ethernet connectivity with Power over Ethernet (PoE)
  - Calibration offsets configurable via Home Assistant
  - Environmental compensation for gas readings

---

## 📂 Project Structure

Each project is contained within its own directory to keep configuration, assets, and documentation organized.

```text
.
├── project-name/
│   ├── project-config.yaml
│   └── README.md (optional, for project-specific details)
├── LICENSE
└── README.md
```

---

## 🛠️ Getting Started

### Prerequisites
- [ESPHome](https://esphome.io/) installed locally or running via Home Assistant.
- Python 3.x (if using CLI).

### Compilation and Upload
To compile and upload a project (e.g., rack monitoring), use the following command:

```bash
# Navigate to the project directory
cd rack-monitoring

# Compile and upload
esphome run rack-environment-monitoring.yaml
```

*Note: For Ethernet-based devices like the ESP32-PoE-ISO, ensure you are on the same network or use the USB-Serial interface for the initial flash.*

## 🏢 About Einwohnergemeinde Brienz
These projects are part of the digital infrastructure of Brienz, Switzerland. They are used to monitor and manage local facilities efficiently using open-source hardware and software.

## 📄 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.