# 📘 JC3249W535 – ESPHome Energy Dashboard for Home Assistant

This repository contains a complete ESPHome configuration for the JC3249W535 320×480 display module, integrated with Home Assistant to visualize real-time energy data. It features a custom LVGL-based UI with animated arrows, dynamic color-coded indicators, and responsive widgets that reflect photovoltaic production, bidirectional power flow, and inverter metrics.

![Dashboard preview](https://github.com/user-attachments/assets/f6bd2de3-0f8f-4f59-9c62-26524077f44f)

## Key Features!

🖥️ Native LVGL dashboard rendered on JC3249W535 (ESP32-S3)

⚡ Real-time animation speed driven by sensor values (e.g. power flow)

🌞 Photovoltaic and inverter data visualization

🔄 Bidirectional energy flow indicators with directional arrows

🎨 Color-coded labels based on energy context (import/export, PV active)

📡 Seamless integration with Home Assistant via API


## Hardware Requirements

JC3249W535c
Optional: BME280, inverter with Modbus/MQTT, power meter

## Software Stack

ESPHome (ESP-IDF framework)
Home Assistant (with MQTT or native API)
LVGL 8.4.0
PlatformIO (for local builds)

## How It Works

Sensor values from Home Assistant are fetched via ESPHome.

Arrows animate vertically and horizontally to indicate energy direction.

Animation speed is dynamically calculated as 6000 - sensor_value, clamped to ensure smooth transitions.

Labels recolor based on energy context (e.g. red for import, green for PV export).


## Getting Started

Flash the ESP32-S3 with the provided .yaml using ESPHome CLI.

Connect the device to Home Assistant via API or MQTT.

Configure your sensors in HA (e.g. sensor.inverter_active_power, sensor.bidirectional_energy_meter_power_b).

Watch the dashboard come alive with real-time data and animations.


## 🎬 Demo Videos


### JC3248W535C · Real‑time Energy Monitoring (ESPHome + Home Assistant)

[![Watch on YouTube](https://img.youtube.com/vi/TExtEiJQPeo/hqdefault.jpg)](https://www.youtube.com/shorts/TExtEiJQPeo)

### Old vs. New 
HTTP Request vs. ESPHome 
ESP32-8048S070 vs. JC3248W535C 
Energy Dashboard Showdown

[![Watch on YouTube](https://img.youtube.com/vi/Ba1jKAf0Ffs/hqdefault.jpg)](https://www.youtube.com/shorts/Ba1jKAf0Ffs)
