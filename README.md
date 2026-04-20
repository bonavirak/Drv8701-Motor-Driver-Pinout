# DRV8701 Motor Driver – Pin Configuration

## Overview

This board is a DRV8701-based motor driver designed for 12V DC motors.

Scan this page to quickly understand how to connect and use the board.

---

## Power Connections

* VM → 12V/24V supply
* GND → Power ground
---

## Motor Output

* M- → Motor terminal A
* M+ → Motor terminal B

---

## Control Pins (MCU)

| Pin      | Description                    |
| -------- | ------------------------------ |
| PH | Direction control                    |
| EN | PWM speed control                    |
| nFAULT   | Fault output (active LOW)      |
| SNSOUT   | Current sense (connect to ADC) |

---

## Basic Usage

1. Connect 12V/24V to VM and GND
2. Connect motor to M+ and M-
3. Connect MCU:

   * PWM → EN 
   * Direction → PH
4. Monitor nFAULT for errors
5. (Optional) Read current from SNSOUT

---

## Notes

* Use proper power supply (able to handle motor current)
* Ensure good cooling for high load
* Do not reverse polarity

---

## Documentation

📄 Pinout PDF: (https://github.com/bonavirak/Drv8701-Motor-Driver-Pinout/blob/main/DRV8701_to_STM32_Pinout.pdf)

---

## Author

Bona Virak
