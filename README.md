# OLO Jiggler Firmware — Readme

Welcome to the official user manual for the **OLO Jiggler** firmware. This firmware transforms your ESP32-C3 development board into an advanced Bluetooth Low Energy (BLE) Mouse Jiggler and multi-utility companion device with a gorgeous OLED display interface.

---

## ⚡ Key Features

1. **BLE Mouse Jiggler** — Keeps your computer awake and active using wireless Bluetooth mouse movements. Supports multiple movement patterns:
   - **SLOW**: Subtle, random movements every 60 seconds.
   - **FAST**: Small movements every second.
   - **ZIGZAG / SQUARE / WAVE**: Continuous, automated shapes for visual validation.
2. **Pomodoro Focus Timer** — On-device work sprint timer (25 minutes focus, 5 minutes break) to help you stay productive.
3. **Daily Habit Tracker** — Keep track of tasks or daily habits with a simple counter.
4. **Daily Quote Mode** — Access a library of 100 motivational and developer-focused quotes.
5. **On-Device Games** — Play retro games built specifically for the 128x64 display (Flappy Block, Dino Run, Reaction Test).
6. **WS2812B Status LED Control** (Big version only) — Custom breathing, rainbow, strobe, and solid color status indications.
7. **Web Controller Interface** — Configure settings, sync time, and monitor status from your Google Chrome or Microsoft Edge browser.

---

## 🔧 Installation & Flashing Guide

To flash this firmware to your OLO Bit or ESP32-C3 dev board:

1. Connect the board to your computer using a USB-C data cable.
2. Open the **OLO Jiggler Installer** (`index.html`) in Google Chrome or Microsoft Edge.
3. Select your display hardware type:
   - **0.96" OLED (SSD1306)** for the Small display version.
   - **1.3" OLED (SH110X)** for the Big display version.
4. Click **Connect & Flash** (or **Install**).
5. A browser popup will show the available COM ports. Select your board (usually labeled *USB Serial Device* or *CH343/CP2102*).
6. Follow the on-screen instructions. The installation takes about 60 seconds. Once completed, the board will reboot into the OLO Jiggler software.

---

## 🕹️ Hardware Controls & Navigation

The OLO Jiggler is operated entirely via a single button or touch sensor connected to the board (default is GPIO 1).

### Basic Button Gestures
* **Single Tap**: Scroll through menu items or rotate home screen pages.
* **Double Tap**: Perform an action on the active page (e.g. start/pause Pomodoro timer, increment Habit counter, make the pet eyes look around).
* **Long Press (Hold for >0.6s)**: Select / Enter a menu, toggle settings, or enter/exit the main settings screen.

### Navigation Flow
1. **Home Pages**: Rotate through home pages (Mouse Jiggler status, System Stats, Daily Quote, CPU Temperature, Pomodoro Timer, Pet Eye Animation, Habit Tracker) with a **Single Tap**.
2. **Open Settings**: From any Home page, **Long Press** the button to enter the **Settings Menu**.
3. **Settings Navigation**:
   - **Single Tap** to scroll down the menu list.
   - **Long Press** to change the value of the selected setting or enter a sub-menu.
   - To go back, scroll to the **Back** item at the bottom of the list and **Long Press**, or perform a **Long Press** from the menu.

---

## ⚙️ On-Device Settings

Settings are re-ordered by use cases (most used items first) to make navigation quick and intuitive:

* **Mode**: Toggle the Jiggling pattern (`OFF`, `SLOW`, `FAST`, `ZIGZAG`, `SQUARE`, `WAVE`).
* **Jiggler Timer**: Set an auto-stop countdown for the mouse jiggler. Choose from `30m`, `1h`, `2h`, `3h`, `4h`, or `Never` (runs indefinitely).
* **Games...**: Select and play built-in retro games.
* **Quote Mode**: Display rotating motivational focus quotes.
* **LED Setup...** (Big version only): Customize status LED behaviors (solid color, rainbow, strobe, breathe, or always off).
* **Animation Timer**: Adjust the delay before the display enters the interactive Eye Animations screensaver. Choose from `1m`, `5m`, `10m`, `15m`, `30m`, `1h`, or `Never`.
* **Anim. Delay**: Adjust how frequently screensaver eyes perform looking or blinking motions.
* **Page Anim**: Select transition style between screens (`SLIDE H`, `SLIDE V`, `NONE`).
* **Sound**: Toggle general buzzer beep alerts `ON`/`OFF`.
* **Anim Sound**: Toggle chirp sounds specifically during eye animations `ON`/`OFF`.
* **Invert Disp**: Invert display colors for comfortable night viewing.
* **Reset Tracker**: Reset daily Habit Tracker count back to 0.
* **Factory Reset**: Clears all saved settings from the board's memory and reboots.

---

## ⚡ Web Controller Usage

Connect the Jiggler to your computer via USB and open the Web Controller (`index.html`) to configure it wirelessly or over serial.

### Setup and Connection
1. Click **⚡ Connect via USB Serial** on the landing page.
2. Select your device port and click **Connect**.
3. Once connected, the interface will automatically sync your system time and unlock the controller dashboard.

### Dashboard Tabs
* **⚡ Controller**: Adjust the active Jiggler mode, trigger jump commands to change pages instantly, play buzzer test tones, trigger habit tracker resets, and sync timezone settings.
* **⚙️ Settings**:
  - **General Preferences**: Toggle sound alerts, screensaver eye chirps, display inversion, page slide animations, and active animation timers.
  - **Bluetooth Identity**: Change your device's Bluetooth broadcast name and manufacturer details (default: `"OLO Bit"`, `"Micromaker Labs"`). Changing details saves to memory and restarts the device with a brand-new connection ID so host computers recognize it as a new device.
* **⚡ Flasher**: Re-flash or upgrade the board firmware directly from the web browser.
