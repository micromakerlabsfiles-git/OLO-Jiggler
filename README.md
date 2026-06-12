# OLO Jiggler (By Micromaker Labs)

A sleek, productivity-focused desk companion built on the ESP32-C3 Super Mini. Designed by Micromaker Labs, the OLO Jiggler acts as a Bluetooth Low Energy (BLE) mouse jiggler to keep your workstation active, while also serving as a Pomodoro timer, habit tracker, and interactive desk pet.

## Features
* **BLE Mouse Jiggler:** Undetectable, hardware-free host connection. Features Slow, Fast, Zigzag, Square, and Wave movement modes.
* **Productivity Suite:** Built-in Pomodoro timer (25/5 min splits), daily habit tracker, and 100 rotating focus quotes.
* **Mini-Games:** Flappy Block, Dino Run, and a Reaction Test to kill time during screen breaks.
* **System Diagnostics:** Live CPU load, RAM usage, and internal temperature tracking graph.
* **Web Controller:** A responsive, dark-glass themed (Grey & Vibrant Orange) web interface to configure the device seamlessly via browser.

## Hardware Wiring
| Component | ESP32-C3 Pin |
| :--- | :--- |
| OLED SDA | GPIO 20 |
| OLED SCL | GPIO 21 |
| Passive Buzzer | GPIO 2 |
| Push Button | GPIO 1 |
| Status LED | GPIO 8 (Built-in) |

## Installation & Flashing
You don't need an IDE to install the firmware. Connect your ESP32-C3 to your computer via a data-capable USB-C cable and visit our **[Web Installer Link]** to flash the device directly from your browser. 

## The Web Controller
The companion web app features a modern, glass-morphism UI with a custom `#1e272e` (Dark Grey) and `#ff793f` (Vibrant Orange) palette. It connects to the OLO Bit via Web Bluetooth, allowing you to change animations, adjust timers, and update settings without touching the device.

## Author
Developed by **Micromaker Labs**.
