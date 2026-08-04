# 🛠️ ESP32 CYD Handheld Embedded Development Toolkit (v2.0)

> **A comprehensive, portable electronics lab & multi-tool suite for ESP32 Cheap Yellow Display (CYD / ESP32-2432S028R).**
> 
> **Developed by Samir Alam** 🚀

---

## ⚡ Quick Download & 1-Click Web Flasher

No Arduino IDE required! You can flash the pre-compiled firmware directly from your web browser or download the raw binary.

| Option | Link | Description |
|---|---|---|
| 🌐 **1-Click Web Flasher** | [**Flash Firmware Online**](https://quadever-launcher.onrender.com/flasher?app=1785854326275) | Flash directly via USB using Chrome/Edge (Web Serial) |
| 📦 **Firmware Binary (.bin)** | [**Download Binary File**](https://quadever-launcher.onrender.com/apps/download/1785854326275) | Direct download for esptool.py or OTA Launchers |

---

## 📋 Table of Contents
1. [Overview](#-overview)
2. [Quick Download & Web Flasher](#-quick-download--1-click-web-flasher)
3. [Hardware Requirements & Specifications](#-hardware-requirements--specifications)
4. [Key Features Detailed Overview](#-key-features-detailed-overview)
   - [Core Electronics & Diagnostics Tools](#-core-electronics--diagnostics-tools)
   - [Lab Instruments & Wave Generators](#-lab-instruments--wave-generators)
   - [Daily Handheld Utilities](#-daily-handheld-utilities)
   - [Electronics Reference & Database](#-electronics-reference--database)
   - [Entertainment & Games](#-entertainment--games)
5. [Global Pin Settings (Dynamic Pin Re-routing)](#-global-pin-settings)
6. [Touch Calibration & Shared NVS Sync](#-touch-calibration--nvs-sync)
7. [Installation & Compilation Guide](#-installation--compilation-guide)
8. [Author & Credits](#-author--credits)

---

## 🌟 Overview

The **ESP32 CYD Handheld Embedded Development Toolkit** transforms the low-cost ESP32 Cheap Yellow Display into a Swiss-army knife for electronics hobbyists, embedded engineers, and technicians.

It features over **26 built-in tools**, an intuitive touch GUI, NVS persistent memory, dynamic GPIO pin re-routing, and seamless integration with OTA Launchers.

---

## ✨ Key Features Detailed Overview

### ⚡ Core Electronics & Diagnostics Tools

1. 💻 **UART Serial Monitor**:
   - **Description**: Full-featured hardware UART2 terminal for debugging external microcontrollers or serial sensors.
   - **Features**:
     - Configurable baud rates: 9600, 19200, 38400, 57600, 115200, 230400, 460800, 921600.
     - Terminal Green aesthetic dark theme with color-coded log entries: 🟢 RX (Received Data), 🟡 TX (Sent Data), ⚪ System Messages.
     - ASCII and HEX viewing modes with smooth vertical scrolling & scrollbar thumb.
     - On-screen touch keyboard for sending custom commands.

2. 🔍 **I2C Lab**:
   - **Description**: Comprehensive bus analyzer, device scanner, and register manipulation utility for I2C chips.
   - **Features**:
     - Auto-scans addresses x01 to x7F at 400kHz Fast Mode.
     - Auto-detects famous sensors/display ICs: OLED (0x3C/0x3D), LCD (0x27/0x3F), MPU6050/DS3231 (0x68), BME280/BMP280 (0x76/0x77), ADS1115 (0x48), BH1750 (0x23), AT24C32 (0x57).
     - Interactive **Read Register** and **Write Register** modes with Hex/Dec inputs.

3. 🔘 **GPIO Lab**:
   - **Description**: Hardware pin state controller and interactive logic analyzer for test points and onboard components.
   - **Features**:
     - Control & inspect 7 pins simultaneously: IO27, IO22, IO35, IO34, IO04 (Red LED), IO16 (Green LED), IO17 (Blue LED).
     - Real-time pin modes: INPUT, OUTPUT, INPUT_PULLUP, INPUT_PULLDOWN.
     - Live high/low status indicators with instant touch toggle for output states.

4. 🌊 **PWM Generator**:
   - **Description**: Versatile pulse-width modulation pulse engine for driving motors, servos, LEDs, and buzzers.
   - **Features**:
     - Adjustable frequency (1Hz – 100kHz) and duty cycle (0% – 100%).
     - **Servo Mode**: 50Hz control with manual slider and automatic sweeping animation.
     - **Motor Control Mode**: Forward/Reverse direction toggle with variable speed control.
     - **LED Dimmer Mode**: Smooth 0-100% brightness control.
     - **Buzzer Note Player**: Plays musical scale tones (C4 to C5).

5. 📈 **Logic Probe**:
   - **Description**: Digital logic level analyzer with live digital waveform plotting.
   - **Features**:
     - Samples digital signals up to 120 buffer samples at 15ms intervals.
     - Automatically measures transition edges to estimate signal frequency in Hz.
     - Detects states: HIGH (1), LOW (0), or PULSING.

6. 📊 **ADC Sensor Dashboard**:
   - **Description**: Multi-channel analog signal viewer for monitoring sensor voltages and onboard telemetry.
   - **Features**:
     - Multi-channel analog plotting for 6 data channels:
       - **CH1**: Probe Pin (IO35)
       - **CH2**: LDR Light Sensor (IO34)
       - **CH3**: CN1 TX Pin (IO27)
       - **CH4**: DAC Output Pin (IO26)
       - **CH5**: ESP32 Internal Hall Effect Sensor
       - **CH6**: ESP32 Internal CPU Temperature Sensor (°C)
     - Live min, max, average voltage measurements with smooth graphing.

---

### 🔬 Lab Instruments & Wave Generators

7. 📉 **Oscilloscope Lite**:
   - **Description**: Portable single-channel analog storage oscilloscope for inspecting AC/DC waveforms.
   - **Features**:
     - 240-sample real-time buffer with 11dB ADC attenuation (3.3V full scale range).
     - Selectable timebases: 100us, 200us, 500us, 1ms, 2ms, 5ms, 10ms, 20ms, 50ms per division.
     - Trigger modes: AUTO and NORM with rising edge trigger detection.
     - On-screen grid lines, voltage reference labels, and STOP/RUN freeze buffer control.

8. 🌐 **Network Toolbox**:
   - **Description**: Complete suite for wireless networking, network diagnostics, and connectivity.
   - **Features**:
     - **WiFi Scanner**: Scans nearby APs with live RSSI signal strength bars.
     - **WiFi AP Connector**: Connects to WPA/WPA2 networks using the virtual touch keyboard.
     - **IP Ping Tool**: Sends ICMP ping packets to check host reachability.
     - **Subnet Scanner**: Auto-discovers active devices connected to your local network.

9. ⚡ **Signal Generator (Sig Gen)**:
   - **Description**: High-speed hardware DAC function generator driving precision analog waveforms.
   - **Features**:
     - Driven by 100kHz hardware interrupt timer for ultra-smooth wave synthesis on GPIO 25/26.
     - **8 Waveforms**: Sine, Triangle, Square, Sawtooth, Half-Sine, Full-Sine, Step, Reverse-Step.
     - Frequency adjustment from 10Hz to 20,000Hz, amplitude scale from 0.0V to 3.3V, and variable duty cycle.

---

### 🧮 Daily Handheld Utilities

10. 🔢 **Calculator**:
    - **Description**: Full-featured pocket scientific calculator designed for quick lab calculations.
    - **Features**:
      - 4x5 button matrix with double-wide  key, decimal ., equals =, Clear C, and percentage %.
      - Floating-point operation, operator chaining, and live calculation history string.

11. ⚖️ **Unit Converter**:
    - **Description**: Multi-category conversion utility for physical engineering units.
    - **Features**:
      - **Temperature**: Celsius (°C), Fahrenheit (°F), Kelvin (K).
      - **Length**: Meters (m), Feet (ft), Inches (in), Centimeters (cm).
      - **Weight**: Kilograms (kg), Pounds (lb), Ounces (oz).

12. ⏱️ **Stopwatch**:
    - **Description**: Anti-flicker precision digital stopwatch with lap timing.
    - **Features**:
      - Centisecond resolution (0:00.00) with 20fps display throttle for flicker-free reading.
      - Tracks up to 8 individual lap times with full lap history log.

13. ⌛ **Countdown Timer**:
    - **Description**: Configurable countdown timer with progress ring meter.
    - **Features**:
      - Set minutes and seconds with simple +/- touch controls.
      - Animated circular progress indicator with audible and visual completion alarm.

14. 📝 **Notes App**:
    - **Description**: Portable text editor for recording pinouts, ideas, and test logs.
    - **Features**:
      - Read, create, edit, and delete .txt notes saved directly to MicroSD card (/toolkit/notes/).
      - Full virtual touch keyboard integration.

15. 🔳 **QR Code Generator**:
    - **Description**: On-screen matrix renderer for generating scannable QR codes.
    - **Features**:
      - Encodes any text, URL, or WiFi credentials into a high-contrast QR code on the TFT screen.

---

### 📚 Electronics Reference & Database

16. 📖 **Component Encyclopedia**:
    - **Description**: Offline component handbook stored in memory & SD card.
    - **Features**:
      - Pinouts, voltage specs, and circuit diagrams for Resistors, Capacitors, Diodes, Transistors, Regulators, and Op-Amps.

17. 💻 **MCU Pinout DB**:
    - **Description**: Interactive pinout viewer for microcontrollers.
    - **Features**:
      - Pin mapping charts for ESP32 CYD, ESP8266 NodeMCU, Arduino Uno/Nano, Raspberry Pi Pico, and STM32 Blue Pill.

18. 🛠️ **Wiring Assist**:
    - **Description**: Visual schematic assistant for hooking up peripherals.
    - **Features**:
      - Step-by-step wiring guides for I2C displays, SPI devices, Servos, Relays, Stepper Drivers, and Sensors.

---

### 🎮 Entertainment & Games

19. 🎨 **Retro Paint**:
    - **Description**: Freehand digital sketchpad.
    - **Features**:
      - Multiple pen thicknesses, color swatches, fill tool, and clear screen.

20. 👾 **Pixel Art Editor**:
    - **Description**: Grid-based 8-bit sprite design tool.
    - **Features**:
      - 20×20 pixel grid with 20-color preset palette, erase mode, clear canvas, and **Custom RGB Color Picker** sliders (R, G, B 0-255).

21. 🐍 **Snake Game**:
    - **Description**: Classic arcade snake game.
    - **Features**:
      - 15×15 grid board, directional touch D-pad, progressive speed, and high score tracking.

22. 🧩 **Tetris Game**:
    - **Description**: Block-stacking puzzle game.
    - **Features**:
      - Falling tetromino pieces, rotation button, left/right drop touch controls, line clearing, and score tracker.

23. 🐤 **Flappy Bird**:
    - **Description**: Fast-paced arcade tap-to-flap game.
    - **Features**:
      - Tuned responsive bird physics (gravity, flap thrust), dynamic scrolling pipes, fair gap clearance (85px), and best score memory.

---

## ⚙️ Global Pin Settings

To change hardware pin assignments without re-compiling:
1. Open **Launcher Page 4 (Electronics)** → Tap **Settings**.
2. Scroll to the desired pin (e.g., Serial RX, I2C SDA, Probe Pin).
3. Use - / + buttons or tap # / value box to type exact GPIO pin.
4. Tap **Save & Apply**. Changes save to NVS and immediately take effect!

---

## 🎯 Touch Calibration & NVS Sync

The toolkit uses the "sys" NVS namespace:
- **Re-calibration**: To re-calibrate inside Toolkit, open **Page 4 (Electronics)** → **Calibrate** → Tap the 4 corner targets carefully.

---

## 👨‍💻 Developed By Samir Alam

---
