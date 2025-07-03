# Lab 10: 4-bit Binary Counter with 74HC161

## 🔍 Objective

This lab focuses on building and testing a **4-bit binary counter** using the **74HC161 IC**, allowing manual load of any 4-bit value and automatic counting via a **555 timer**-generated clock.

---

## 🧪 Part A: Counter with Load Function

### 🔧 Learning Goals

- Understand the 74HC161 counter IC pinout and behavior.
- Use the **LD** pin to load a custom 4-bit value into the counter.
- Observe 4-bit binary output on LEDs.
- Generate a clock using **555 timer**.

### 🧱 Components

- 74HC161 Counter IC
- LMC555 Timer IC
- DIP4 switch
- SPST push button
- Yellow LED (clock debug)
- 4 Red LEDs (counter output)
- 330Ω and 10kΩ resistors
- 1MΩ trimpot
- 1µF capacitor
- Breadboard, jumper wires
- 3V battery pack

### 📐 Pin Summary

- **Input**: A (Pin 3), B (Pin 4), C (Pin 5), D (Pin 6)
- **Load**: LD (Pin 9) ← active low push button
- **Clock**: CLK (Pin 2) ← from 555 timer
- **Output**: QA–QD → 4 red LEDs
- **Control**: CLR (Pin1), ENP, ENT tied high or unused

### ⚙️ Implementation Steps

1. Build and test 555 timer for clock (yellow LED blinks).
2. Connect DIP switch to A–D pins with pull-ups.
3. Wire 74HC161 CLK input to timer output.
4. Wire LD pin through push button to GND.
5. Display output on LEDs from QA–QD.
6. Load custom value and observe counting behavior.

### ⚠️ Notes

- LD is active-low: press button to load value from DIP.
- Outputs cycle from 0000 → 1111 with clock pulses.
- Don’t reverse Vcc and GND on ICs.
- Use LEDs to validate each binary value.

---

## ✅ Outcomes

- Successfully observed 4-bit counter incrementing with each clock tick.
- Verified correct LOAD functionality for values: 0010, 1010, 1111, 1001.
- Learned to debug digital counters using visual LED output.
