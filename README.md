# OLO Jiggler (By Micromaker Labs)

A sleek, productivity-focused desk companion and Web Serial Controller built on the **ESP32-C3 Super Mini**. Designed by Micromaker Labs, the OLO Jiggler acts as a Bluetooth Low Energy (BLE) mouse jiggler to keep your workstation active, while also serving as a Pomodoro timer, habit tracker, interactive desk pet, and synchronized desktop clock.

---

## ✨ Features

- **📶 Dual-Purpose Web Tool (`index.html`)**:
  - **Firmware Installer**: Flash SSD1306 (Small) or SH110X (Big) firmware directly from the browser using WebUSB.
  - **Device Controller**: Control the Jiggler in real-time via Web Serial (jump to pages, toggle modes, play buzzer tones, trigger habit tracker resets, and send automated clock sync commands).
- **🖱️ BLE Mouse Jiggler**: Undetectable wireless jiggler with multiple movement behaviors: Slow, Fast, Zigzag, Square, and Wave modes.
- **🕒 Background Clock Sync**: Syncs host PC time in the background (including timezone offsets). A minimalistic Clock screen is automatically displayed on the device when a USB serial connection is active.
- **🌈 WS2812B Status NeoPixel**: Capped strictly at **50% brightness** to prevent damage. Color-coded animations flash/breathe dynamically based on the active jiggle mode. Includes override options for custom Solid, Rainbow, Breathe, Strobe, or Off effects.
- **🛠️ Dynamic Pins Configuration**: Customize hardware pins (SDA, SCL, Touch, Buzzer, NeoPixel) dynamically from the Web Controller. Saves directly to device preferences and reboots instantly.
- **🎮 Built-in Retro Games**: Flappy Block, Dino Run, and Reaction Test.
- **📚 Productivity Suite & Diagnostics**: Pomodoro timer (25/5 split), 100 focus quotes, daily habit tracker, and live CPU/RAM temperature tracking graphs.

---

## 🔌 Default Hardware Pins

Pins are reconfigurable, but defaults are loaded as:

| Component | Default GPIO Pin |
| :--- | :--- |
| **OLED SDA** | GPIO 20 |
| **OLED SCL** | GPIO 21 |
| **Touch Button** | GPIO 1 |
| **Passive Buzzer** | GPIO 2 |
| **WS2812B LED** | GPIO 6 |

---

## 📦 Installation & Flashing

Connect your ESP32-C3 SuperMini to your computer via a data-capable USB-C cable and visit the [**Web Installer & Controller**](index.html) to flash the firmware and manage settings directly.

---

## 🛠️ Authors & Credits

Developed by **Micromaker Labs**.
- ESP32-BLE-Mouse by T-vK
- Adafruit SH110X & SSD1306 Libraries
- U8g2_for_Adafruit_GFX
