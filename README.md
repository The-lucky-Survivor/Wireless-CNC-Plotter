# Wireless CNC Plotter

Welcome to the **Wireless CNC Plotter** repository! This project details the step-by-step construction, software setup, and usage of an Arduino-based CNC drawing robot. Whether you're looking to build your own drawing machine or understand the technical aspects of the custom CNC Master app, this repository has everything you need from A to Z.

---

## 🚀 Project Overview

The Wireless CNC Plotter (DrawBot) uses an Arduino Uno, a CNC Shield, and GRBL firmware to control stepper motors and a servo for drawing. It is based on a robust structural design and integrates with custom software tailored for ease of use and precision.

Here is what you will find in this repository:
- **3D Printed Parts:** All the STL files required to build the mechanical structure.
- **Documentation:** Full assembly guides and technical explanations.
- **Firmware & Scripts:** The GRBL `config.h` and the servo Python script.
- **Media:** Photos and videos showing the working robot and assembly results.
- **G-Code Examples:** Ready-to-use G-Code files to test your robot right away.

---

## 📁 Repository Structure

* `3D_Printed_Parts/` - Contains all `.stl` files needed to 3D print the robot chassis, clamps, and pen holders. 
* `Documentation/` - Contains the primary user guides and technical materials:
  * `DrawBotAssemblyUserGuideV3.pdf` - Your A-Z guide for physical assembly.
  * `CNC Master Technical Documentation Overview.pptx` - Deep dive into the custom App that commands the CNC.
* `Firmware/` - Key files for compiling GRBL (`config.h`) and Inkscape servo extensions (`servo.py`).
* `Media/` - High-quality photos (`Images/`) and videos (`Videos/`) of the final project and parts. Included is also the website's QR code.
* `GCode_Examples/` - Some sample `.gcode` drawings to test your machine (e.g., Minnie Mouse, geometric shapes, etc).

---

## 🛠️ Getting Started (A-Z Guide)

### 1. Mechanical Assembly
Open the [DrawBot Assembly User Guide](Documentation/DrawBotAssemblyUserGuideV3.pdf). This document provides a highly detailed walkthrough of the physical build, including required hardware (rods, bearings, belts, M3/M8 nuts and bolts) and how to assemble the 3D-printed parts.

### 2. Electronics Setup
You will need:
- Arduino Uno
- CNC Shield (with 3 jumpers installed per stepper driver)
- 2x A4988 Stepper Drivers
- 2x NEMA 17 Stepper Motors
- 1x SG90 Servo (for Z-axis pen up/down)
- 12V 2A Power Supply

*Important:* Make sure to set the stepper drivers' current correctly to avoid skipped steps or overheating.

### 3. Firmware (GRBL)
Flash the Arduino Uno with the custom GRBL firmware.
1. Download the GRBL servo library.
2. **Crucial Step:** Replace the default `config.h` in the downloaded library with the `config.h` found in the `Firmware/` directory of this repo. This enables the CoreXY kinematics. (If you skip this, your robot will draw at a 45-degree angle!).
3. Upload to your Arduino via the Arduino IDE.

### 4. Software & Control
You have multiple ways to generate drawings and control the plotter. The provided PPTX (`CNC Master Technical Documentation Overview.pptx`) details the robust app designed to run the plotter. 

Alternatively, to build drawings manually:
1. Install Inkscape v0.92 with Python 3.7.x.
2. Use the MI GRBL Extension to convert `.svg` to G-Code. (Use the `servo.py` file inside `Firmware/` if you encounter Python errors).
3. Connect using Universal G-Code Sender (UGS) or the custom app to begin drawing.

---

## 📸 Media & Results

Check out the robot in action below!

### 🖼️ Gallery
<p align="center">
  <img src="Media/Images/WhatsApp%20Image%202026-04-20%20at%2001.48.23.jpeg" width="32%" alt="Robot Photo 1">
  <img src="Media/Images/WhatsApp%20Image%202026-04-20%20at%2013.48.24.jpeg" width="32%" alt="Robot Photo 2">
  <img src="Media/Images/WhatsApp%20Image%202026-04-20%20at%2013.48.32.jpeg" width="32%" alt="Robot Photo 3">
</p>

### 🎥 Video Demonstration
<video src="Media/Videos/WhatsApp%20Video%202026-04-20%20at%2001.21.01.mp4" controls="controls" width="100%"></video>

* **More Info:** You can find all drawings, components, and clips directly in the `Media/` folder.

---

## 📱 Learn More (Website QR Code)

Scan the QR code below or open `Media/Images/QR for the website.jpg` to visit the official website, featuring in-depth tutorials, software downloads, and more!

*(Attach QR Image here)*
![Website QR Code](Media/Images/QR%20for%20the%20website.jpg)

---

## 📜 Credits & License
This repository combines resources to streamline the building process. Modified for the **Wireless CNC Plotter** GitHub repository.

For full source and updates, visit: [Wireless-CNC-Plotter on GitHub](https://github.com/The-lucky-Survivor/Wireless-CNC-Plotter/tree/main)
