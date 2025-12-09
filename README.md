# mynew.html - SmartSwitch Web UI

This is a standalone HTML file that serves as a complete web-based user interface for controlling an ESP32-based smart lighting system. The interface connects to the device through Blynk REST API and provides comprehensive control over lighting, sensors, and device settings.

## Features

### Lighting Control
- Control up to 8 individual lights/relays
- Visual feedback with animated bulb icons
- Customizable light names
- Grid layout with responsive design

### Lighting Modes
- **Teaching Mode**: Turns on all lights
- **Projector Mode**: Configurable preset for projector use
- **Energy Saver Mode**: Configurable preset for energy saving

### Scheduling & Timers
- Schedule lighting scenes for specific time periods
- Set timers for individual lights
- Clear existing schedules and timers

### Sensor Management
- PIR motion sensor configuration
- RCWL microwave radar sensor settings
- Adjustable sensor parameters (delay, range)
- Presence detection status display

### WiFi & Device Management
- WiFi network configuration and management
- Blynk integration for remote access
- Device notifications and status monitoring
- Connection status visualization

### Tools & Diagnostics
- Device restart functionality
- Log viewing and clearing
- Configuration export
- Terminal communication with device

## How to Use

1. Open `mynew.html` in a web browser
2. Enter your Blynk authentication token in the Settings > Tools section
3. Click "Connect" to establish connection with your device
4. Control lights directly from the Home tab
5. Configure modes, schedules, and sensors using the respective tabs

## Technical Details

### Architecture
- Standalone HTML file with embedded CSS and JavaScript
- Uses Blynk REST API for device communication
- Local storage for persisting UI settings
- Responsive design that works on desktop and mobile devices

### Blynk Integration
- Connects to Blynk Cloud via REST API
- Uses virtual pins for device communication:
  - V0-V7: Individual light controls
  - V8: UI heartbeat
  - V9: ESP device status
  - V10: Presence detection
  - V11: PIR sensor enable/disable
  - V12: RCWL sensor enable/disable
  - V20: Current mode indicator
  - V25: Terminal communication
  - V30-V32: WiFi configuration

### Security
- Blynk token encryption using XOR cipher with device fingerprint
- Client-side only - no server dependencies
- Secure local storage of settings

## UI Components

### Navigation
- **Home**: Main lighting controls and mode selectors
- **Timer**: Scheduling and timer management
- **Settings**: Sensor configuration, light renaming, and tools

### Visual Design
- Dark theme with gradient backgrounds
- Animated icons and interactive elements
- Responsive layout for all screen sizes
- Real-time status indicators

## Requirements

- Modern web browser (Chrome, Firefox, Safari, Edge)
- Internet connection for Blynk communication
- ESP32 device running compatible firmware
- Blynk account with valid authentication token

## File Information

- **Size**: ~2,370 lines
- **Structure**: Single HTML file with embedded CSS and JavaScript
- **Dependencies**: None (standalone)
- **Compatibility**: Works locally without web server
