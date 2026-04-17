# DRV8701 Motor Driver – Pin Configuration

## Overview

This board is a DRV8701-based motor driver designed for 12V DC motors.

Scan this page to quickly understand how to connect and use the board.

---

## Power Connections

* VM → 12V supply
* GND → Power ground
* DVDD → Logic supply (3.3V / 5V)

---

## Motor Output

* OUT1 → Motor terminal A
* OUT2 → Motor terminal B

---

## Control Pins (MCU)

| Pin      | Description                    |
| -------- | ------------------------------ |
| IN1 / PH | Direction control              |
| IN2 / EN | PWM speed control              |
| nFAULT   | Fault output (active LOW)      |
| SNSOUT   | Current sense (connect to ADC) |

---

## Basic Usage

1. Connect 12V to VM and GND
2. Connect motor to OUT1 and OUT2
3. Connect MCU:

   * PWM → EN / IN2
   * Direction → IN1 / PH
4. Monitor nFAULT for errors
5. (Optional) Read current from SNSOUT

---

## Notes

* Use proper power supply (able to handle motor current)
* Ensure good cooling for high load
* Do not reverse polarity

---

## Documentation

📄 Pinout PDF: (upload your PDF in repo and link here)

---

## Author

Bona Virak
