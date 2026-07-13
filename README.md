# 🤖 DeshBot Smart Robotic Kit
### Bluetooth Controlled Arduino Robot Car with Intelligent Obstacle Avoidance

![Arduino](https://img.shields.io/badge/Arduino-Nano-00979D?logo=arduino)
![Language](https://img.shields.io/badge/Language-C++-00599C?logo=cplusplus)
![Platform](https://img.shields.io/badge/Platform-Arduino_IDE-blue)
![License](https://img.shields.io/badge/License-MIT-green)

## 📌 Overview

DeshBot is an intelligent Arduino Nano-based robotic vehicle that combines **Bluetooth manual control** with an **automatic safety override system**.

The robot receives movement commands from a smartphone via the HC-05 Bluetooth module. At the same time, an HC-SR04 ultrasonic sensor continuously monitors the surroundings. If an obstacle is detected within the predefined safety distance, the Arduino automatically overrides the user's command, preventing collisions by stopping and changing direction.

A 16×2 LCD provides real-time information about robot status and obstacle distance.

---

## ✨ Features

- 📱 Bluetooth control using HC-05
- 🚧 Automatic obstacle detection
- 🛡️ Safety Override System
- 📟 Live distance display on 16×2 LCD
- 🚗 Forward, Backward, Left & Right movement
- ⚡ Arduino Nano based
- 🔋 Battery powered motor system
- 🎯 Beginner-friendly robotics project

---

# 🛠 Hardware Components

| Component | Quantity |
|-----------|----------|
| Arduino Nano | 1 |
| DeshBot Development Board | 1 |
| HC-05 Bluetooth Module | 1 |
| HC-SR04 Ultrasonic Sensor | 1 |
| L298N Motor Driver | 1 |
| 16x2 LCD Display | 1 |
| DC Gear Motors | 2 |
| Robot Chassis | 1 |
| Lithium Battery | 1 |

---

# ⚙ Working Principle

The project works in two modes simultaneously.

### Manual Mode

- Smartphone sends commands via Bluetooth.
- HC-05 receives the command.
- Arduino executes movement.

Supported commands:

| Command | Action |
|---------|--------|
| `f` | Forward |
| `b` | Backward |
| `l` | Left |
| `r` | Right |
| `s` | Stop |

---

### Safety Override Mode

The HC-SR04 continuously measures the distance ahead.

If:

```
Distance < 20 cm
```

The Arduino:

- Stops the motors
- Displays obstacle warning
- Turns automatically
- Continues driving safely

This prevents collisions even if the user keeps pressing the Forward button.

---

# 📊 System Architecture

```
 Smartphone
      │
 Bluetooth
      │
    HC-05
      │
 Arduino Nano
      │
 ┌───────────────┐
 │               │
LCD          Ultrasonic
Display        Sensor
 │               │
 └──────┬────────┘
        │
   L298N Driver
        │
     DC Motors
```

---

# 🔌 Pin Configuration

## Ultrasonic Sensor

| Sensor Pin | Arduino Pin |
|------------|-------------|
| Trig | D12 |
| Echo | D2 |
| VCC | 5V |
| GND | GND |

### LCD

```
RS -> A4
EN -> A3
D4 -> A2
D5 -> A1
D6 -> A0
D7 -> D13
```

### Motor Driver

| Function | Arduino Pin |
|----------|-------------|
| Left Motor 1 | D6 |
| Left Motor 2 | D7 |
| Right Motor 1 | D8 |
| Right Motor 2 | D9 |

---

# 🚀 Installation

1. Clone this repository

```bash
git clone https://github.com/yourusername/DeshBot.git
```

2. Open the project in Arduino IDE.

3. Install the required library:

```
LiquidCrystal
```

4. Connect Arduino Nano.

5. Remove the HC-05 module while uploading the code.

6. Upload the sketch.

7. Reconnect the HC-05 module.

8. Pair your phone with HC-05.

9. Open any Bluetooth Terminal Controller application.

10. Start driving!

---

# 📷 Demo

You can add:

- Images
- Circuit Diagram
- GIF
- Working Video

inside this section.

Example:

```
/Images
/Circuit
/Demo
```

---

# 📂 Project Structure

```
DeshBot/
│
├── Arduino_Code/
│      DeshBot.ino
│
├── Documentation/
│      Documentation.pdf
│
├── Images/
│
├── Circuit/
│
├── LICENSE
│
└── README.md
```

---

# 💡 Future Improvements

- Mobile App
- Voice Control
- Line Following Mode
- Wi-Fi Control using ESP32
- Camera Streaming
- IoT Monitoring
- Autonomous Navigation
- GPS Integration

---

# 📚 Technologies Used

- Arduino Nano
- Embedded C++
- Arduino IDE
- HC-05 Bluetooth
- HC-SR04 Ultrasonic Sensor
- LCD Interface
- Motor Driver (L298N)

---

# 📖 Learning Outcomes

This project demonstrates:

- Embedded Systems
- Robotics
- Sensor Interfacing
- Bluetooth Communication
- Motor Control
- Obstacle Avoidance
- Real-Time Decision Making

---

# 🤝 Contributing

Contributions are welcome!

If you have ideas to improve the project, feel free to fork the repository and submit a Pull Request.

---

# 📄 License

This project is licensed under the MIT License.

---

# 👨‍💻 Author

**Nikat Parihar**

B.Tech Electronics & Communication Engineering

Model Institute of Engineering & Technology (MIET), Jammu

---

⭐ If you found this project useful, consider giving the repository a **Star**!
