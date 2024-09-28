# BMP280 Sensor Readings using ESP32

This repository contains an Arduino code to interface the BMP280 sensor using the ESP32 microcontroller via I2C communication. The code reads temperature, pressure, and altitude from the sensor and prints them to the serial monitor.

## Table of Contents
- [Introduction](#introduction)
- [Hardware Requirements](#hardware-requirements)
- [Software Requirements](#software-requirements)
- [Setup Instructions](#setup-instructions)
- [Code Overview](#code-overview)
- [Usage](#usage)

## Introduction
The BMP280 is a barometric pressure sensor that can measure temperature, pressure, and estimate altitude. This project uses the ESP32 to read data from the BMP280 sensor and display it on the serial monitor.

## Hardware Requirements
- **ESP32 microcontroller**
- **BMP280 sensor**
- Breadboard and jumper wires

### Pin Connections:
| BMP280 Pin | ESP32 Pin |
|------------|-----------|
| VCC        | 3.3V      |
| GND        | GND       |
| SCL        | GPIO 22   |
| SDA        | GPIO 21   |

## Software Requirements
- [Arduino IDE](https://www.arduino.cc/en/Main/Software) with ESP32 board support installed
- Adafruit BMP280 library: Install it from the Arduino Library Manager by searching for "Adafruit BMP280"

## Setup Instructions
1. Connect the BMP280 sensor to the ESP32 using I2C (refer to the hardware requirements section for pin connections).
2. Open the Arduino IDE and install the necessary libraries (Adafruit BMP280).
3. Upload the code to your ESP32 using the Arduino IDE.
4. Open the serial monitor to view temperature, pressure, and altitude data.

## Code Overview
- The BMP280 sensor is initialized using I2C communication.
- Default sensor settings are applied with oversampling for temperature and pressure.
- Temperature, pressure, and estimated altitude values are printed every 2 seconds.

### Key Functions:
- `bmp.begin(0x76)`: Initializes the BMP280 sensor at address 0x76.
- `bmp.readTemperature()`: Reads the temperature in Celsius.
- `bmp.readPressure()`: Reads the pressure in Pascals.
- `bmp.readAltitude()`: Calculates the altitude based on the current pressure and reference sea-level pressure.

## Usage
1. Power the ESP32 and BMP280 sensor.
2. Open the serial monitor to view the live temperature, pressure, and altitude data.
