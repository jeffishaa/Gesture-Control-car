# 🚗 Gesture Control Car using ESP32 & MPU6050

A wireless **Gesture-Controlled Robot Car** built using **ESP32** and the **MPU6050 Gyroscope & Accelerometer Sensor**. The car is controlled by simple hand movements instead of a traditional joystick or mobile application.

The transmitter unit reads hand gestures using the MPU6050 sensor and sends movement commands wirelessly to the receiver ESP32. The receiver controls the motors through a motor driver, allowing the car to move in real time. This approach is commonly implemented using ESP-NOW for low-latency communication. :contentReference[oaicite:0]{index=0}

---

## 📌 Features

- 🎮 Hand gesture-based wireless control
- 📡 ESP-NOW communication between two ESP32 boards
- ⚡ Low latency and fast response
- 🚗 Forward, Backward, Left, Right, and Stop movements
- 🔋 Battery-powered portable design
- 🛠 Easy to modify and expand

---

## 🧰 Components Required

| Component | Quantity |
|-----------|----------|
| ESP32 Development Board | 2 |
| MPU6050 Gyroscope & Accelerometer | 1 |
| L298N/L293D Motor Driver | 1 |
| DC Geared Motors | 2 or 4 |
| Robot Chassis | 1 |
| Wheels | 2 or 4 |
| Battery Pack (7.4V/11.1V) | 1 |
| Jumper Wires | As required |
| Power Switch | 1 |

---

## 📂 Project Structure

```
Gesture-Control-Car/
│
├── Transmitter/
│   └── transmitter.ino
│
├── Receiver/
│   └── receiver.ino
│
├── Circuit_Diagram/
│   └── wiring.png
│
├── Images/
│   ├── transmitter.jpg
│   ├── receiver.jpg
│   └── demo.gif
│
└── README.md
```

---

## ⚙️ Working Principle

1. The MPU6050 detects the tilt of the user's hand.
2. ESP32 reads accelerometer and gyroscope data.
3. The data is converted into movement commands.
4. Commands are transmitted wirelessly using ESP-NOW.
5. The receiver ESP32 receives the command.
6. The motor driver drives the motors accordingly.

---

## 🎯 Gesture Mapping

| Hand Gesture | Car Movement |
|--------------|--------------|
| Tilt Forward | Move Forward |
| Tilt Backward | Move Backward |
| Tilt Left | Turn Left |
| Tilt Right | Turn Right |
| Keep Hand Flat | Stop |

---

## 🔌 Circuit Connections

### Transmitter (ESP32 + MPU6050)

| MPU6050 | ESP32 |
|---------|-------|
| VCC | 3.3V |
| GND | GND |
| SDA | GPIO21 |
| SCL | GPIO22 |

---

### Receiver (ESP32 + L298N)

| ESP32 | L298N |
|--------|--------|
| GPIO26 | IN1 |
| GPIO27 | IN2 |
| GPIO14 | IN3 |
| GPIO12 | IN4 |
| GND | GND |

> **Note:** Pin assignments can be modified in the code.

---

## 📥 Required Libraries

Install the following libraries in the Arduino IDE:

- WiFi.h
- esp_now.h
- Wire.h
- Adafruit MPU6050
- Adafruit Unified Sensor

---

## 🚀 Installation

1. Clone this repository.

```bash
git clone https://github.com/yourusername/Gesture-Control-Car.git
```

2. Open the **Transmitter** sketch.
3. Upload it to the transmitter ESP32.
4. Open the **Receiver** sketch.
5. Upload it to the receiver ESP32.
6. Update the receiver MAC address in the transmitter code.
7. Power both ESP32 boards.
8. Tilt your hand to control the robot.

---

## 📸 Project Images

Add your project images here.

```
Images/
├── transmitter.jpg
├── receiver.jpg
├── wiring.png
└── demo.gif
```

---

## 📊 Applications

- Robotics
- Industrial automation
- Gesture-controlled vehicles
- Assistive technologies
- Educational projects
- Wireless control systems

---

## 🔮 Future Improvements

- Obstacle avoidance using Ultrasonic Sensor
- Speed control using PWM
- OLED display
- Battery monitoring
- Voice control
- Mobile app integration
- AI gesture recognition

---

## 🐞 Troubleshooting

**ESP-NOW not connecting**
- Verify both MAC addresses.
- Ensure both ESP32 boards use the same Wi-Fi channel.

**MPU6050 not detected**
- Check SDA and SCL connections.
- Verify I2C address (0x68 or 0x69).

**Motors not moving**
- Check battery voltage.
- Verify motor driver wiring.
- Confirm enable pins are active.

---

## 📈 Project Flow

```
Hand Gesture
      │
      ▼
 MPU6050 Sensor
      │
      ▼
 ESP32 (Transmitter)
      │
 ESP-NOW Wireless
      │
      ▼
 ESP32 (Receiver)
      │
      ▼
 Motor Driver
      │
      ▼
 Robot Car Movement
```

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push the branch
5. Open a Pull Request

---

## 📜 License

This project is licensed under the MIT License.

---

## 👨‍💻 Author

**Your Name**

GitHub: https://github.com/yourusername

---

## ⭐ Support

If you found this project helpful, please consider giving it a **⭐ Star** on GitHub.

Happy Coding! 🚀
