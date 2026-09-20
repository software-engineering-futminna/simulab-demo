# ETH / LabSys 402: Engineering Virtual Laboratory
> **Swiss Deep Blue Edition** — An interactive, zero-dependency browser-based engineering simulator for hardware architectures, discrete digital logic, structured cabling, and net-centric communications.

---

## 📋 Overview

The **Engineering Virtual Laboratory** is a comprehensive hardware and systems engineering simulator built with an uncompromising Dieter Rams / Swiss International Style aesthetic. It offers four fully interactive workstations covering core computer science and hardware laboratory syllabi:

1. **Workstation 01: Logic & Proto-Board** — Discrete TTL 74LS-series digital logic circuit design and dual-channel oscilloscope analysis.
2. **Workstation 02: PC Architecture** — Motherboard component integration, jumper configuration, ACPI power sequencing, BIOS POST diagnostics, and an interactive Linux hardware shell.
3. **Workstation 03: Cabling & Punch-Down** — ANSI/TIA-568.2-D Cat 6 UTP cable termination (T568A / T568B), 110 IDC punch-down patch panel rack, and 8-channel automated wire map testing.
4. **Workstation 04: Net-Centric & Radio** — Network topology simulation, packet injection (ICMP/TCP/UDP), 433/915 MHz RF transceivers, and Hayes AT dialup/PABX modem handshakes.

---

## 🖥️ Workstations & Features

### 01. Logic & Proto-Board
- **Component Palette**:
  - **Inputs & Clock**: Binary Toggle Switches (`0 / 1`), Master Clock Generator (`0.1 Hz – 50 Hz`), and manual step pulser.
  - **Discrete Logic Gates (TTL 74LS)**: `AND` (74LS08), `OR` (74LS32), `NAND` (74LS00), `NOR` (74LS02), `XOR` (74LS86), and `NOT Inverter` (74LS04).
  - **Outputs & Probes**: Logic LED Indicators with realistic glow shading, Oscilloscope Channel 1 (`Y1 Amber`), and Channel 2 (`Y2 Cyan`) test probes.
- **Interactive Breadboard**: Click-to-route point-to-point jumper wires, drag-and-drop IC positioning, and live multi-pass circuit evaluation.
- **Prebuilt Presets**:
  - `2-to-1 Multiplexer (MUX)`
  - `Master-Slave JK Flip-Flop`
  - `Half-Adder (Sum XOR + Carry AND)`
- **Dual-Trace Oscilloscope**: Real-time signal graphing, voltage scale adjustments (`0.5V/DIV` to `10.0V/DIV`), timebase controls, hold mode, and 1 kHz calibration reference.

### 02. PC Architecture & Diagnostics
- **Modular Hardware Configuration**:
  - Install/remove CPU cooler, RAM modules (DDR4), SATA SSD, ATAPI CD-ROM, and Display monitor.
  - Interactive HDD Master/Slave and Clear-CMOS jumper blocks.
- **System Sequencing**:
  - ACPI Power toggle (`POWER ON / OFF`).
  - Active CPU fan spinning animation (`fan-spin`).
  - Realistic BIOS POST sequence with diagnostic beeps synthesized via Web Audio API.
  - Dynamic CPU thermal modeling and tachometer RPM tracking.
- **Embedded Hardware Shell (`syslab-host`)**:
  - `lshw` — Detailed hardware hierarchy inspection
  - `lspci` — PCI bus bridge and controller enumeration
  - `uname -a` — Kernel version identification
  - `dmesg` — Kernel ring buffer and boot diagnostics
  - `cat /proc/cpuinfo` — CPU architecture, cache, and frequency
  - `free -h`, `lsblk`, `df -h` — Memory and storage partition stats
  - `ifconfig`, `arp -a`, `traceroute`, `ping` — Network interface diagnostics

### 03. Cabling & 110 Punch-Down
- **ANSI/TIA-568.2-D Cat 6 Specifications**:
  - Terminate Connector A and Connector B independently with **T568A** or **T568B** standards.
  - Wire color-coding: White-Green, Green, White-Orange, Blue, White-Blue, Orange, White-Brown, Brown.
- **Fault Presets**: Straight-Through, Crossover, and Split-Pair fault scenarios.
- **Automated LAN Cable Tester (T-800)**:
  - 8-channel sequential pulse sweep with synchronized TX/RX LED indicators.
  - Pin-by-pin continuity diagnostic logging and pass/fail verdict detection.
- **24-Port 19" Rack Patch Panel**: Interactive punch-down block termination with status indicators.

### 04. Net-Centric & Radio Systems
- **Topology Canvas**: Drag-and-drop networked hosts (Linux / Windows), L2 switches, L3 gateway routers, radio APs, and PABX exchange units.
- **Live Cable Patching**: Interactive point-to-point link creation and deletion.
- **Packet Injection**: Simulate ICMP Ping, TCP SYN, and UDP datagram transit across subnets.
- **Sub-GHz Radio Transceiver**: Selectable RF carriers (`433 MHz`, `868 MHz`, `915 MHz`), RSSI dBm signal estimation, and GFSK modulation metrics.
- **PABX & Dialup Emulation**: Realistic Hayes `ATDT` dial sequences and authentic dual-frequency V.34 modem handshake tone synthesis.

---

## ⌨️ Keyboard Shortcuts

| Key | Action |
| :--- | :--- |
| `1` | Switch to **Logic & Proto-Board** |
| `2` | Switch to **PC Architecture** |
| `3` | Switch to **Cabling & Punch-Down** |
| `4` | Switch to **Net-Centric & Radio** |
| `P` | Toggle side diagnostic panel (Oscilloscope / Hardware Monitor / Cable Tester) |

---

## 🚀 Getting Started

The virtual laboratory is self-contained in a single, portable HTML file with **zero build steps** and **zero external npm dependencies**.

### Option 1: Direct File Launch
Simply double-click or open `engineering_virtual_laboratory.html` in any modern web browser (Chrome, Safari, Firefox, Edge).

### Option 2: Local HTTP Server
Run with Python:
```bash
python3 -m http.server 8080
```
Or with Node / npx:
```bash
npx serve .
```
Then navigate to `http://localhost:8080/engineering_virtual_laboratory.html`.

---

## 🔊 Audio Synthesis
The simulator features sound design built on the **Web Audio API**:
- BIOS POST single beep (OK) and multi-beep error codes (RAM missing, display fault, fan failure).
- Rotary tactile click and wire patch feedback.
- DTMF dual-tone telephone dialing and 33.6 kbps modem handshake frequencies.
- Audio can be muted or unmuted at any time using the **AUDIO ON / MUTED** header toggle button.

---

## 📄 License
Academic & Educational Use — Computer Science & Hardware Engineering Laboratories.
