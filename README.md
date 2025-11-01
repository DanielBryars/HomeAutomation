# Home Automation

A comprehensive home automation project featuring Home Assistant configurations, ESP32 integrations, and custom hardware control implementations.

## Overview

This repository contains configurations, firmware, and custom components for a complete home automation system. It includes Home Assistant setup, ESP32 microcontroller projects, and hardware interface code for controlling various smart home devices.

## Components

### Home Assistant Configuration

Located in `hass/config/`, this includes:

- **configuration.yaml**: Main Home Assistant configuration
- **automations.yaml**: Automated rules and triggers
- **scripts.yaml**: Custom automation scripts
- **groups.yaml**: Device and entity groupings
- **Custom Components**: HACS (Home Assistant Community Store) integration

### Features

- **Lovelace UI**: Custom YAML-based dashboard
- **Text-to-Speech**: Google Translate TTS integration
- **Weather Integration**: DarkSky weather platform
- **Solar Monitoring**: SMA solar inverter integration
- **System Monitoring**: Glances server monitoring dashboard
- **Container Management**: Portainer Docker interface

### ESP32 Projects

The `esp32/` directory contains:

- ESP32 microcontroller projects for IoT devices
- ESP32-POE (Power over Ethernet) implementations
- MCP23S17 GPIO expander integration
- Technical documentation and datasheets

### Hardware Interfaces

#### MCP23S17 GPIO Expander

The `MCP23S17/` directory contains documentation for the MCP23S17 SPI GPIO expander chip, enabling expansion of I/O pins for additional sensors and actuators.

#### Arduino Sketches

`sketch_aug04a/` - OneWire DS18B20 temperature sensor implementation:
- Reads temperature from DS18B20/DS18S20 sensors
- Uses OneWire protocol on pin D4
- Serial output for temperature monitoring

## Technologies Used

- **Home Assistant**: Open-source home automation platform
- **ESP32**: Low-power microcontroller with WiFi/Bluetooth
- **Arduino**: Firmware development for microcontrollers
- **OneWire Protocol**: For temperature sensors
- **SPI**: For GPIO expander communication
- **MQTT**: Message broker for IoT communication (likely)
- **Docker**: For containerized services (Portainer integration)
- **YAML**: Configuration format

## Hardware Components

- Home Assistant server (likely Raspberry Pi or similar)
- ESP32 development boards
- ESP32-POE boards
- MCP23S17 GPIO expander chips
- DS18B20 temperature sensors
- SMA solar inverter
- Various smart home devices

## Setup

### Prerequisites

- Home Assistant installation
- Arduino IDE or PlatformIO for ESP32 development
- ESP32 board support packages
- Required Arduino libraries (OneWire, etc.)

### Installation

1. **Home Assistant Configuration**:
   ```bash
   # Copy configuration files to your Home Assistant config directory
   cp -r hass/config/* /path/to/homeassistant/config/
   ```

2. **ESP32 Firmware**:
   - Open projects in Arduino IDE
   - Install required libraries
   - Configure WiFi credentials
   - Upload to ESP32 boards

3. **Arduino Sensors**:
   - Install OneWire library
   - Connect DS18B20 sensor to pin D4 with 4.7K pull-up resistor
   - Upload sketch to Arduino board

## Configuration Notes

- Update IP addresses in configuration.yaml to match your network
- Set up secrets.yaml for sensitive information (API keys, passwords)
- Configure HACS token for custom component access
- Adjust sensor pins and configurations based on your hardware

## Integrations

- **Solar Monitoring**: SMA inverter at 192.168.1.104
- **System Monitoring**: Glances at 192.168.1.106:61208
- **Container Management**: Portainer at 192.168.1.106:9000
- **Weather**: DarkSky API integration
- **HACS**: Custom components, themes, and Python scripts

## Security Notes

Remember to:
- Move sensitive tokens and API keys to secrets.yaml
- Use strong passwords for all services
- Keep Home Assistant and integrations updated
- Secure network access to automation services

## Future Enhancements

- Additional sensor integrations
- More complex automation rules
- Voice control integration
- Energy monitoring and optimization
- Camera/security system integration

## Status

Active home automation system with ongoing development and improvements.
