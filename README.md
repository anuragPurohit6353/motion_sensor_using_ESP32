# 📷 ESP32-CAM Motion Sensor with Telegram Alerts

A smart surveillance project using an ESP32-CAM and a PIR motion sensor to detect motion, capture images, and send them directly to a Telegram bot for remote monitoring.

## 🚀 Features

- Detects motion using a PIR sensor.
- Captures a photo instantly when motion is detected.
- Sends the photo to your Telegram bot.
- Lightweight and ideal for home automation or security systems.
- Sends humidity/temperature (optional) if using DHT11 or similar sensor.

---

## 🧰 Components Used

| Component             | Quantity |
|----------------------|----------|
| ESP32-CAM Module      | 1        |
| PIR Motion Sensor     | 1        |
| FTDI Programmer       | 1        |
| Jumper Wires          | As needed|
| (Optional) DHT11/DHT22| 1        |

---

## 🔌 Circuit Diagram

![Circuit Diagram](images/circuit_diagram.png)

> 📌 **Note**: Connect `PIR OUT` to GPIO pin used in code (commonly GPIO 13 or 14).

---

## 💻 How It Works

1. Motion is detected by the PIR sensor.
2. ESP32-CAM wakes up and captures an image.
3. The captured photo is sent to your specified Telegram bot.
4. (Optional) Humidity/temperature data is also sent.

---

## 🔧 Setup Instructions

1. Clone this repository or download the ZIP.
2. Open `ESP32_CAM_Motion_Telegram.ino` in Arduino IDE.
3. Install the required libraries:
    - `UniversalTelegramBot`
    - `WiFi`
    - `ESP32`
4. Replace the following placeholders in the code:
    - `WIFI_SSID` and `WIFI_PASSWORD`
    - `TELEGRAM_BOT_TOKEN`
    - `CHAT_ID` (your Telegram user or group ID)

5. Connect ESP32-CAM via FTDI and upload the code.
6. Press the **RST** button after upload to run.

---

## 📷 Output Example

Photo sent to Telegram bot when motion is detected:

![Example Photo](images/example_output.jpg)

---

## 📁 Folder Structure

