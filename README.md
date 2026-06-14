# Smart Medication Reminder System

An Arduino-based medication reminder system that uses a real-time clock (RTC), LCD display, voice alerts, and a confirmation button to help users remember and confirm taking their medication.

---

## Project Overview

This project reminds the user to take medication using:

- Arduino UNO
- DS3231 RTC Module
- LCD 16x2 I2C Display
- DFPlayer Mini (MP3-TF-16P V3.0)
- Speakers
- Push Button

### Features

- Real-time clock using DS3231
- LCD display for time and status
- Voice medication reminders
- Continuous alarm until confirmation
- Simple and low-cost design
- Easy to customize

---

## Hardware Components

| Component | Quantity |
|------------|----------|
| Arduino UNO | 1 |
| DS3231 RTC Module | 1 |
| LCD 16x2 I2C Display | 1 |
| DFPlayer Mini MP3 Module | 1 |
| Speaker 4Ω 10W | 2 |
| Push Button | 1 |
| 1kΩ Resistor | 1 |
| 5V 1A Power Adapter | 1 |
| Micro SD Card | 1 |

---

## Wiring Connections

### DFPlayer Mini

| DFPlayer | Arduino |
|-----------|----------|
| VCC | 5V |
| GND | GND |
| RX | D11 (through 1kΩ resistor) |
| TX | D10 |
| SPK1 | Speaker + |
| SPK2 | Speaker - |

### DS3231 RTC

| DS3231 | Arduino |
|---------|----------|
| VCC | 5V |
| GND | GND |
| SDA | A4 |
| SCL | A5 |

### LCD I2C

| LCD | Arduino |
|------|----------|
| VCC | 5V |
| GND | GND |
| SDA | A4 |
| SCL | A5 |

### Push Button

| Button | Arduino |
|---------|----------|
| One Side | D2 |
| Other Side | GND |

---

## Required Libraries

- Wire
- RTClib
- LiquidCrystal_I2C
- SoftwareSerial
- DFRobotDFPlayerMini

---

## Audio File Setup

1. Format the SD card as FAT32.
2. Copy your reminder audio file.
3. Rename it to:

0001.mp3

4. Insert the card into the DFPlayer Mini.

---

## System Workflow

Start → Display Time → Reminder Triggered → Play Voice Alert → Wait for Button Press → Stop Alert → Confirm Dose → Return to Monitoring

---

## Future Improvements

- Multiple medication schedules
- ESP32 Wi-Fi notifications
- Mobile App integration
- SMS reminders
- Medication history logging

---

## Author

**Eng. Gharieb Aref**

Instrumentation & Control Systems Engineer

Python Programming Instructor

Embedded Systems Enthusiast

---

## License

MIT License
