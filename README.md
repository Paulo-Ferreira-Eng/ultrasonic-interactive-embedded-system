Ultrasonic Interactive Embedded System
Overview

This project implements a simple interactive embedded system using an ultrasonic sensor and an OLED display.
The system continuously measures distance using an HC-SR04 sensor and controls an animated character rendered on a 128x64 OLED display. The animation runs normally when no object is detected and stops when an object is within a predefined distance threshold.

Objective

The purpose of this project is to demonstrate:

- integration of sensor input with real-time visual output

- distance measurement using an ultrasonic sensor

- basic state-based behavior in an embedded system

- rendering bitmap animation on an OLED display

System Description
The system operates by measuring distance through the ultrasonic sensor:

- A trigger pulse is sent from the microcontroller

- The echo response is measured to calculate distance

- The measured value is compared against a fixed threshold

Behavior:

- If distance > threshold → animation runs

- If distance ≤ threshold → animation stops

This creates a simple reactive interaction between the user and the system.

Hardware Components

- Microcontroller (Arduino or compatible)

- Ultrasonic sensor (HC-SR04)

- OLED display (128x64, SSD1306)

- Basic wiring and power supply

Software Implementation

- Display control is handled using Adafruit_GFX and Adafruit_SSD1306 libraries

- Communication with the display is done via I2C (Wire)

- Animation frames are stored in program memory (PROGMEM)

- Distance is calculated based on pulse duration from the ultrasonic sensor

- System behavior is controlled through a simple conditional structure based on distance threshold

Results

The system provides consistent real-time response to distance changes, with immediate visual feedback on the display.

The animation control behaves as expected, demonstrating reliable interaction between sensor input and graphical output.

Limitations

- Fixed distance threshold (hardcoded)

- Single sensor input

- No filtering or smoothing of distance readings

- No modular code structure

- No power optimization

Possible Improvements

- Implement adjustable or dynamic distance threshold

- Add filtering to improve measurement stability

- Refactor code into modular structure

- Expand animation system with additional states

- Optimize performance and memory usage

Notes

This project was developed as a practical experiment in embedded systems, focusing on real-time interaction between physical input and visual feedback.

The visual behavior is inspired by retro game mechanics and used as a reference for interaction design.
