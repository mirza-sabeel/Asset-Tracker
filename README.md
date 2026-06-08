# BMA400 Asset Protection System

A low-power asset tamper detection system using the BMA400 
accelerometer. Detects physical disturbance and triggers 
an alert via buzzer and LED.

## How It Works
1. BMA400 reads acceleration on X, Y, Z axes every second
2. Current reading compared against previous baseline values
3. If the difference exceeds the threshold — disturbance detected
4. Buzzer and LED flash 5 times as alert
5. Baseline resets to new position after movement
6. System returns to low-power polling state

## Features
- I2C interfacing with BMA400 using SparkFun library
- Threshold-based motion detection (adjustable sensitivity)
- Buzzer + LED alert on disturbance
- Low-power polling design (1 second interval)
- Serial monitor logging for debugging

## Hardware Used
- Arduino (ATmega328P)
- BMA400 Accelerometer (Bosch) — I2C address 0x14 or 0x15
- Buzzer (Pin 8)
- LED (Pin 9)

## Adjustable Parameters
- `threshold` — controls sensitivity (default 0.05g). 
   Lower value = more sensitive to small movements.
- `delay(1000)` — polling interval in milliseconds.

## Tech Stack
- Embedded C (Arduino framework)
- I2C protocol
- SparkFun BMA400 Arduino Library

## Developed During
Internship at Vivartan Technologies LLP (Jan 2026 – May 2026)
