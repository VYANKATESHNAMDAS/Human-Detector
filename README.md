# 🔐 Human-Detector System using ESP32-CAM | Face Recognition + Telegram Alert 📷📩

This project is a smart security solution that uses the **ESP32-CAM** module to detect motion using a **PIR sensor**, perform **face recognition**, and send an alert image to **Telegram** if an **unknown face** is detected.

## 📌 Features

- 📸 Motion Detection using PIR Sensor
- 🧠 Face Recognition using ESP32-CAM
- 📤 Automatic alert photo sent to Telegram
- 💡 Optimized for low power and real-time use
- 📶 Wi-Fi based communication

---

## 🔧 Hardware Requirements

| Component        | Quantity |
|------------------|----------|
| ESP32-CAM (AI Thinker) | 1        |
| PIR Motion Sensor (HC-SR501) | 1        |
| FTDI USB-to-Serial Adapter | 1        |
| Jumper Wires     | As needed |
| Breadboard (Optional) | 1        |

---

## 🔌 Circuit Diagram

| ESP32-CAM Pin | PIR Sensor Pin |
|---------------|----------------|
| 5V            | VCC            |
| GND           | GND            |
| GPIO13        | OUT            |

> Note: Connect GPIO0 to GND only during uploading.

---

## 🔐 Software Requirements

- Arduino IDE
- ESP32 Board Package ([Installation Guide](https://randomnerdtutorials.com/installing-the-esp32-board-in-arduino-ide-windows-instructions/))
- Libraries:
  - `WiFi.h`
  - `WiFiClientSecure.h`
  - `esp_camera.h`
  - `UniversalTelegramBot`
  - `esp32_face_recognition.h` *(or custom face matching logic)*

---

## 🤖 How It Works

1. The PIR sensor detects motion.
2. ESP32-CAM captures an image.
3. The captured face is checked against known faces.
4. If the face is **unknown**, the image is sent to your **Telegram bot**.
5. You receive a live alert with a photo on your phone.

---

## 📱 Telegram Bot Setup

1. Open Telegram and search for `@BotFather`
2. Send `/newbot` and follow the instructions to get your `BOT_TOKEN`
3. Start the bot and use this URL to find your `chat_id`:  
