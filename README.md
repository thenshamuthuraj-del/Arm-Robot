# 🤖 IoT Robotic Arm Controlled via Blynk (ESP8266)

An ESP8266-based robotic arm with **five servo motors**, remotely controlled using the **Blynk IoT platform**.  
This project demonstrates real-time IoT control of multiple actuators—ideal for learning, demos, or prototyping automation systems.

---

## 📦 **Features**
✅ Control five servo motors via smartphone  
✅ Simple Blynk dashboard integration  
✅ Wi-Fi enabled using NodeMCU (ESP8266)  
✅ Clean, minimal code for easy customization

---

## 🛠 **Hardware Used**
- NodeMCU ESP8266
- 5× Servo motors (e.g., SG90)
- USB power supply / external 5V power for servos
- Jumper wires

---

## ⚙️ **Pin Configuration**

| Servo | ESP8266 Pin |
|------:|:-----------:|
|  1    | D2          |
|  2    | D3          |
|  3    | D5          |
|  4    | D6          |
|  5    | D7          |

*(You can adjust these pins in the code if needed.)*

---

## 📲 **Blynk Setup**
- Use the new **Blynk IoT** app (not the legacy one)
- Create 5 sliders:
  - `V0` → controls Servo 1  
  - `V1` → controls Servo 2  
  - `V2` → controls Servo 3  
  - `V3` → controls Servo 4  
  - `V4` → controls Servo 5
- Each slider:  
  - Range: `0–180` (servo angle)
  - Send on release: enabled

---

## 🧰 **Libraries Used**
- `ESP8266WiFi.h`
- `BlynkSimpleEsp8266.h`
- `Servo.h`
