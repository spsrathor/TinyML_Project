# TinyML Keyword Spotting Project

A voice-controlled LED system using TinyML on Arduino Nano 33 BLE Sense microcontroller. This project demonstrates real-time keyword spotting using Edge Impulse machine learning models for voice recognition.

Name - **Surya Pratap Singh Singh**

Matriculation Number - **638278**

## 🎯 Project Overview

This project implements two voice-controlled systems:
1. **Simple ON/OFF Control** - Basic LED control using "ON" and "OFF" commands
2. **Multiple Commands** - Extended control with "ON", "OFF", "UP", and "DOWN" commands

The system uses machine learning models trained with Edge Impulse to recognize spoken keywords and control an onboard LED in real-time.

## Hardware Requirements

- **Arduino Nano 33 BLE Sense** (with built-in microphone)
- USB cable for programming and power
- Computer with Arduino IDE

## Software Requirements

- **Arduino IDE**
- **Edge Impulse Libraries**:
  - `ei-keyword_spotting-arduino-1.0.2.zip` (for on_off project ***Model A***)
  - `ei-multiple_voice-arduino-1.0.1.zip` (for multiple_cmds project ***Model B***)


### Install Edge Impulse Libraries
1. In Arduino IDE, go to **Sketch > Include Library > Add .ZIP Library**
2. Select and install the provided Edge Impulse library files:
   - `ei-keyword_spotting-arduino-1.0.2.zip` -  ***Model A***
   - `ei-multiple_voice-arduino-1.0.1.zip` - ***Model B***

### Upload the Code
1. Connect your Arduino Nano 33 BLE Sense to your computer
2. Select the correct board: **Tools > Board > Arduino Nano 33 BLE**
3. Select the correct port: **Tools > Port > [Your Arduino Port]**
4. Choose one of the projects:
   - For basic control: Open `on_off/on_off/on_off.ino`
   - For multiple commands: Open `multiple_cmds/multiple_cmds/multiple_cmds.ino`
5. Click **Upload**

## Usage

### Project 1: ON/OFF Control (`on_off/` - Model A)
- **"ON"** - Turns the LED on
- **"OFF"** - Turns the LED off

### Project 2: Multiple Commands (`multiple_cmds/` - Model B)
- **"ON"** or **"UP"** - Turns the LED on
- **"OFF"** or **"DOWN"** - Turns the LED off

### Testing the System
1. Open the Serial Monitor (Tools > Serial Monitor) at 115200 baud
2. Wait for the system to initialize
3. Speak clearly into the microphone
4. Observe the LED changes and serial output showing prediction confidence

### Machine Learning Models
- **Framework**: TensorFlow Lite for Microcontrollers
- **Training Platform**: Edge Impulse
- **Model Type**: Neural Network for audio classification
- **Classes**: 
  - **Model A** - Two voice commands model: ["ON", "OFF"]
  - **Model B** - Four voice commands model: ["ON", "OFF", "UP", "DOWN"]