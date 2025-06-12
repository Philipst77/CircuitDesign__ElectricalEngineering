# 💡 Dual-LED Circuit with Breadboard Nets – Lab 2

## 📌 Objective
Build a dual-LED circuit using a breadboard and understand how **electrically identical nets** work. This lab introduces fundamental breadboarding concepts such as **dual power rails** and the concept of a **net**—points that are electrically identical but physically separated.

---

## 🧪 Components Used
- 🔋 3V Battery Pack  
- 🔴 Red LED  
- 🟢 Green LED  
- ⚡ Two 330Ω Resistors  
- 🧵 Jumper wires  
- 🔲 Breadboard  

---

## 🧰 Circuit Overview
This lab builds a simple circuit with **two LEDs** (red and green), each protected by a **330Ω resistor**. Power is supplied via a **3V battery**, and current flows when the battery is switched ON.

- Red and Green LEDs each connect in series with a resistor.
- The anodes are connected to **Vcc**, and cathodes to **GND**.
- The circuit consumes approximately **12 mW** total.

---

## 🔌 Breadboard Strategy
To maximize space and connectivity:

- ✅ Connect the **top Vcc rail** to the **bottom Vcc rail** using a jumper.
- ✅ Connect the **top GND rail** to the **bottom GND rail** using another jumper.

This configuration creates **unified power rails** on both sides of the board, simplifying circuit expansion and layout.

---

## 🔄 Understanding “Nets”
A **net** is a set of points in a circuit that are **electrically identical**, even if physically spread out. Key nets in this circuit include:

- **Net α / σ / φ** → Connect battery ground and both LED cathodes to GND
- **Net β / γ / δ** → Connect battery Vcc and both resistors' top pins to power rail
- **Net μ / ε** → Link each resistor bottom pin to each LED anode

This layout enables proper current flow with minimal wiring.

---

## 🧠 Key Concepts Illustrated
- 🧲 Nets allow cleaner circuit layout by logically grouping connections.
- 🔁 Current flows from **positive to negative**, powering LEDs.
- 🔋 Rails can be shared across the breadboard for better layout efficiency.
- ⚠️ **Do not connect battery terminals directly**—this will drain the battery rapidly.

---

## 🧪 Prototype Highlights
- Red LED cathode is wired to **Top GND rail**.
- Green LED cathode is wired to **Bottom GND rail**.
- Shared breadboard rows are used to connect anodes and resistors.

---

## ✅ Completion Indicator
When the circuit is correctly built and powered:
- 🔴 **Red LED is ON**
- 🟢 **Green LED is ON**

> 💬 **Tip:** Always switch off the battery pack when not in use to preserve energy.

---
