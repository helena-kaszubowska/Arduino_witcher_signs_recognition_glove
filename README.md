# Witcher Signs Glove

Arduino project for recognizing hand gestures inspired by signs from *The Witcher*.  
The glove uses five flex sensors to detect finger bending, an MPU6050 accelerometer/gyroscope module to detect hand orientation, and an SSD1306 OLED display to show the recognized sign.

## Features

- Recognition of hand gestures inspired by Witcher signs
- Support for signs such as Aard, Igni, Quen, Axii and Yrden
- Finger bending detection using five flex sensors
- Hand orientation detection using the MPU6050 motion sensor
- OLED display output with sign names and bitmap symbols
- Additional custom messages displayed for selected gestures
- Gesture stabilization using smoothing and hysteresis

## Hardware

- ESP32-S expansion board
- 5 flex sensors
- MPU6050 accelerometer and gyroscope module
- SSD1306 OLED display, 128x64 px
- Jumper wires

## Technologies

- Arduino IDE
- C/C++
- Adafruit SSD1306 library
- Adafruit GFX library
- Adafruit MPU6050 library
- Adafruit Unified Sensor library
- Wire library

## How it works

The program reads analog values from five flex sensors placed on the fingers.  
The sensor values are mapped to percentage values and smoothed using an exponential moving average filter.

The MPU6050 module is used to read acceleration data and determine the orientation of the hand.  
Based on the combination of finger positions and hand orientation, the program detects a specific gesture and displays the corresponding Witcher sign or message on the OLED screen.

## Detected gestures

- Aard
- Igni
- Quen
- Axii
- Yrden
- Custom text-based gestures

## File structure

- `Witcher_Signs.ino` — main Arduino sketch 

## Notes

The flex sensor threshold values are calibrated for a specific glove setup.  
If the hardware setup changes, the calibration values may need to be adjusted in the code.
