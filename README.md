# 🤖 Obstacle Avoiding Robot (Arduino)

This project is an **autonomous obstacle-avoiding robot** built using **Arduino**, an **ultrasonic sensor**, a **servo motor**, and **DC motors**.
The robot detects obstacles in front of it and automatically decides whether to turn left or right to avoid collisions.

---

## 📌 Features

* 🚗 Moves forward automatically
* 📡 Detects obstacles using an ultrasonic sensor
* 🔄 Servo motor rotates the sensor to scan left and right
* 🧠 Chooses the direction with more free space
* ⚡ Smooth motor speed control using PWM
* 🔁 Fully autonomous.

---

## 🧰 Components Used

* Arduino (Uno / Nano / compatible)
* Ultrasonic Sensor (HC-SR04)
* Servo Motor
* DC Motors (2)
* Motor Driver (L298N / L293D)
* Robot chassis
* Battery / Power supply
* Connecting wires

---

## 🔌 Pin Connections

### Ultrasonic Sensor

| Sensor Pin | Arduino Pin |
| ---------- | ----------- |
| TRIG       | A0          |
| ECHO       | A1          |

### Servo Motor

| Servo Pin | Arduino Pin |
| --------- | ----------- |
| Signal    | 10          |

### Motor Driver

**Left Motor**

| Pin | Arduino |
| --- | ------- |
| IN1 | 5       |
| IN2 | 4       |
| ENA | 6 (PWM) |

**Right Motor**

| Pin | Arduino |
| --- | ------- |
| IN3 | 7       |
| IN4 | 8       |
| ENB | 9 (PWM) |

---

## 📚 Libraries Required

Install these libraries in the Arduino IDE:

* **NewPing**
* **Servo** (built-in)

### How to Install

1. Open Arduino IDE
2. Go to **Sketch → Include Library → Manage Libraries**
3. Search for **NewPing** and install it

---

## ⚙️ How It Works

1. Robot moves forward continuously
2. Ultrasonic sensor checks distance ahead
3. If an obstacle is detected within **15 cm**:

   * Robot stops
   * Moves backward briefly
   * Servo rotates the sensor to the right and left
   * Compares distances
4. Robot turns toward the direction with more space
5. Continues moving forward

---

## 🧪 Code Overview

* `readPing()` → Measures distance using ultrasonic sensor
* `lookLeft()` / `lookRight()` → Scans surroundings using servo
* `moveForward()` / `moveBackward()` → Controls movement
* `turnLeft()` / `turnRight()` → Avoids obstacles
* PWM is used for smooth motor speed control

---

## ▶️ How to Upload the Code

1. Open the `.ino` file in Arduino IDE
2. Connect Arduino to your computer
3. Select the correct **Board** and **Port**
4. Click **Upload**
5. Power the robot and place it on the ground

---

## 🚀 Future Improvements

* Add Bluetooth or WiFi control
* Improve turning accuracy
* Add LCD or LED status indicators
* Use multiple sensors for better detection
* Add speed control mode.

## 👤 Author

**MONISHA C M**
GitHub: [https://github.com/MonishaCM155](https://github.com/MonishaCM155)

---

## 📜 License

This project is open-source and free to use for learning and educational purposes.

