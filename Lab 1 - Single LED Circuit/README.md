# 🔴 LED Circuit Lab – Simple Current-Limiting Design

## 🧠 Objectives

- Understand and interpret circuit schematics (Vcc, GND).
- Learn the role and function of basic electronic components:
  - Resistors
  - Light Emitting Diodes (LEDs)
  - Power supplies
- Build a basic LED circuit on a breadboard using:
  - A 330Ω resistor
  - A red LED
  - A 3V battery pack
- Gain hands-on experience with breadboard prototyping.

---

## 🧩 Components Used

| Element       | Type     | Value         |
|---------------|----------|---------------|
| Resistor      | Fixed    | 330Ω          |
| LED           | Diode    | Red           |
| Power Source  | Battery  | 3V (2x AA)     |
| Breadboard    | Prototyping tool | N/A |

---

## 🔧 Circuit Design Overview

The goal is to light up a red LED safely using a 330Ω resistor to limit current from a 3V battery pack.

### 🔌 Key Circuit Principles

- **Resistor** limits the current to around 3 mA to protect the LED.
- **LED** only conducts in one direction (forward-biased) and emits visible red light.
- **3V Battery Pack** provides power (Vcc = 3V, GND = 0V).
- **Breadboard** enables modular, reusable, and clean connections.

---

## 📝 Schematic Summary

The schematic consists of:

[+3V] ---- [330Ω Resistor] ---->|---- [GND]
LED


- The resistor and LED are connected in series.
- The LED's **anode** connects to the resistor.
- The **cathode** of the LED connects to GND.

---

## 🧪 Breadboard Setup Instructions

1. **Insert Batteries** into the pack (flat end = negative, pointy end = positive).
2. **Connect RED wire** from the battery pack to the breadboard’s top Vcc rail.
3. **Connect BLACK wire** to the top GND rail.
4. Insert:
   - One end of the **resistor** to Vcc rail.
   - Other end of **resistor** to row 6D.
   - **Anode** of LED to row 6A.
   - **Cathode** of LED to any hole in the GND rail.

👉 *Row 6 is chosen because its columns (A–E) are internally connected.*

---

## ⚠️ Safety and Power Tips

- Always **turn OFF** the battery pack when the circuit is not in use.
- Avoid **shorting** Vcc and GND wires — it could cause heat or fire.
- **Don’t hardwire** components — always use the breadboard to preserve part integrity.

---

## ✅ Expected Outcome

Once the connections are made and the battery pack is switched ON:
- The red LED will light up safely without burning out.
- You have successfully prototyped a basic electronic circuit!

---

## 📷 Demo

![LED Circuit](insert-your-image-url-here)

---

## 📚 Learn More

- [Resistor Color Code – Wikipedia](https://en.wikipedia.org/wiki/Electronic_color_code#Resistor_code)
- [How LEDs Work – Wikipedia](https://en.wikipedia.org/wiki/Light-emitting_diode)
