# OLO Jiggler — User Manual & Operating Guide

Welcome to the official user manual for **OLO Jiggler** by Micromaker Labs. This guide explains all end-user features, touch gesture controls, menu navigation, display configuration, and Web Controller usage.

---

## ⚡ Key Features

1. **🖱️ BLE Mouse Jiggler**: Keeps host computers awake over Bluetooth Low Energy with multiple movement patterns:
   - **SLOW**: Subtle movement every 60 seconds (stealthy & undetectable).
   - **FAST**: Micro movements every second.
   - **ZIGZAG / SQUARE / WAVE**: Continuous geometric movement shapes for visual verification.
2. **⏱️ Jiggler Auto-Stop Timer**: Automatically stops mouse movement after a set duration (`30m`, `1h`, `2h`, `3h`, `4h`, or `Never`).
3. **📺 NVS Display Type Selection**: Choose between **SH110X (1.3" OLED)** and **SSD1306 (0.96" OLED)** display types directly from the Web Controller or Serial commands. Settings save to NVS preferences across reboots.
4. **🔌 Customizable Pinouts**: Remap hardware GPIO pins (I2C SDA, I2C SCL, Touch Button, Buzzer, NeoPixel LED) wirelessly or over USB Serial. Saved directly to NVS memory.
5. **💡 Smart NeoPixel Status LED**: Color-coded lighting indications (capped at 50% brightness for hardware protection). Auto-disabled when SSD1306 display type is selected.
6. **📱 Borderless OS UI & Touch Dot**: Clean borderless interface with a small touch indicator dot at the bottom right corner `(x=125, y=61)` whenever input touch/press is active.
7. **⏱️ Productivity & Utility Suite**:
   - **Pomodoro Timer**: 25-minute work sprint and 5-minute break cycle.
   - **Daily Habit Tracker**: Track daily habits or task counters on screen.
   - **Daily Focus Quotes**: 100 motivational quotes for developers and makers.
   - **CPU & RAM Diagnostics**: Live real-time temperature tracking graphs.
8. **🎮 Built-in Retro Games**: Flappy Block, Dino Run, and Reaction Test.

---

## 🕹️ Hardware Touch Controls & Gestures

OLO Jiggler is controlled via a single touch sensor or physical button on the dev board:

| Touch Gesture | Action |
|---|---|
| **Single Tap** | Scroll down menu items or cycle through Home Screen pages. |
| **Double Tap** | Perform active page action (Start/Pause Pomodoro, increment Habit counter, trigger eye animation motions). |
| **Long Press (>0.6s)** | Enter/Select a menu item, toggle a setting value, or return back to Home Screen. |

> [!TIP]
> Whenever a touch or button press is registered, a small **touch dot** lights up in the bottom-right corner `(x=125, y=61)` of the display.

---

## 🌐 Web Controller Guide (`index.html`)

Open `index.html` in any Web Serial compatible browser (**Google Chrome** or **Microsoft Edge**) and click **🔌 Connect via USB Serial**.

### Dashboard Tabs Overview

1. **⚡ Jiggler Controls**:
   - Instantly switch active Jiggle Mode (`NONE`, `SLOW`, `FAST`, `ZIGZAG`, `SQUARE`, `WAVE`).
   - Quick jump buttons (0 to 7) to open any display page remotely.
   - Play buzzer test tones and reset the habit tracker.
2. **⚙️ Settings & Pins**:
   - **Display Type Selection**: Switch between `SH110X (1.3" OLED)` and `SSD1306 (0.96" OLED)`. Saves to NVS preferences and reboots the board cleanly.
   - **Hardware GPIO Pinouts**: Remap I2C SDA, I2C SCL, Button, Buzzer, and NeoPixel pins.
   - **System Preferences**: Toggle general audio beeps, eye animation chirps, display color inversion, and page slide transition animations (`SLIDE H`, `SLIDE V`, `NONE`).
3. **🌐 BLE & Timers**:
   - **Bluetooth Identity**: Change BLE device broadcast name (default: `"OLO Bit"`) and manufacturer details (default: `"Micromaker Labs"`). Automatically re-calculates host MAC address offsets so host PCs treat it as a brand-new device.
   - **Timers**: Set Screensaver activation timeout, Jiggler auto-stop timer, and Eye animation delays.
   - **Clock Sync**: Enable automatic background time sync or force manual RTC sync with custom timezone offsets.
4. **💡 NeoPixel LED**:
   - Configure override lighting effects (`Solid Color`, `Rainbow Cycle`, `Breathing Pulse`, `Strobe Flash`, or `Always OFF`).
   - Drag Red, Green, and Blue sliders with real-time color preview box.
   - *Note: Automatically disabled when SSD1306 display type is selected.*
5. **🔧 Web Flasher**:
   - Flash pre-compiled firmware binaries directly to your ESP32-C3 board over USB without installing Python or command-line tools.
6. **💻 Serial Event Console**:
   - Monitor real-time RX/TX command logs, status payloads, and hardware diagnostic messages.

---

## 🔧 Flashing & Firmware Upgrade

1. Connect your ESP32-C3 board to your computer using a data USB-C cable.
2. Open `index.html` in Google Chrome or MS Edge.
3. On the landing page or **Web Flasher** tab, choose your display target:
   - **SH110X** for 1.3" displays with NeoPixel status LED.
   - **SSD1306** for 0.96" compact displays.
4. Click **Install OLO Jiggler Firmware** (or **Connect & Flash**).
5. Select your COM port from the browser pop-up. If unrecognised, hold the physical **BOOT** button on the board while plugging in the USB cable.

---

## ❓ Frequently Asked Questions (FAQ)

- **Q: How do I know if touch input is working?**  
  A: Look at the bottom-right corner of the OLED display — a tiny touch indicator dot appears whenever touch input is active.
- **Q: Can I change display hardware without re-flashing?**  
  A: Yes! Open the Web Controller, go to **Settings & Pins**, select your Display Type (`SH110X` or `SSD1306`), and click Save. The setting will save to NVS preferences and reboot the board.
- **Q: How do I pair OLO Jiggler with a new computer?**  
  A: Change the BLE Device Name or Manufacturer in the **BLE & Timers** tab. The firmware computes a unique MAC address offset upon reboot so your computer sees it as a brand-new Bluetooth device.
