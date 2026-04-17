# DRV8701 Motor Driver PCB

## General

This project is a high-current DC motor driver based on the DRV8701 gate driver IC.
It is designed for robotics applications such as Robocon, where reliable and efficient motor control is required.

The driver uses external MOSFETs to form an H-bridge, allowing bidirectional control of DC motors with PWM.

---

## Configuration

### Electrical Specifications

* Supply Voltage (VM): 12V (compatible with 3S Li-ion)
* Logic Voltage: 3.3V / 5V
* Driver IC: DRV8701
* Topology: External MOSFET H-Bridge

---

### Control Interface

* PWM input (speed control)
* Direction control (PH/EN)
* nFAULT output (fault monitoring)
* Current sense output (SNSOUT → MCU ADC)

---

### Protection Features

* TVS diode (SMBJ18A) for voltage spike protection
* Reverse polarity protection (MOSFET-based)
* Bulk capacitor for transient suppression
* Proper ground plane design for noise reduction

---

### PCB Design

* 4-layer PCB
* Solid ground plane (low impedance return path)
* Power plane for VM distribution
* Wide copper for high current paths
* Thermal vias under driver IC for heat dissipation

---

## Hardware Files

* `/hardware/kicad` → KiCad schematic and PCB files
* `/docs` → Exported schematics (PDF)
* `/images` → PCB renders and screenshots

---

## Usage

1. Connect power supply (12V) to VM and GND
2. Connect motor to output terminals
3. Provide control signals from MCU:

   * PWM
   * Direction
4. Monitor fault via nFAULT pin
5. (Optional) Read current via SNSOUT

---

## Status

🚧 In development

---

## Future Improvements

* Current limiting tuning
* Thermal performance optimization
* CAN or advanced communication interface

---

## Author

Bona Virak

---

## License

MIT License
