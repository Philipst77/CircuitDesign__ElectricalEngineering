# Lab 9: 8-to-1 Multiplexer with Temperature Sensor LEDs

## 🔍 Objective

This lab demonstrates how to combine 3-bit overlapping temperature sensor inputs to drive green and red LEDs using **NOR gates**, a **74HC151 multiplexer**, and a **555 timer** for flashing logic.

---

## 🧪 Part A: LED Logic with Sensor Data

### 🔧 Learning Goals

- Interpret temperature sensor values using combinational logic.
- Enable/disable LEDs via Initial Decision Maker (NOR gate circuit).
- Use the **74HC151 MUX** to control ON/OFF/FLASHING LED behavior.
- Integrate a 555 timer square wave for flashing control.

### 🧱 Components

- 74HC151 8-to-1 Multiplexer
- 74HC02 Quad NOR Gate
- LMC555 Timer IC
- DIP4 switch (3 used)
- Green, Red, and Yellow LEDs
- 330Ω resistors
- 10kΩ pull-up resistors
- 1MΩ trimpot
- 1µF capacitor
- Breadboard and jumper wires
- 3V battery pack

### 📐 Logic Breakdown

| S3 | S2 | S1 | Meaning        | LED Action    |
|----|----|----|----------------|---------------|
| 0  | 0  | 0  | < 80°F         | Green ON      |
| 0  | 0  | 1  | 80–89°F        | Green FLASH   |
| 0  | 1  | 1  | 80–99°F        | Green & Red   |
| 1  | 0  | 0  | 111–120°F      | Red FLASH     |
| 1  | 1  | 0  | 100–120°F      | Red ON        |
| Others        | Not possible   | All OFF       |

### ⚙️ Implementation Steps

1. Build 555 timer square wave generator and test yellow LED blinking.
2. Wire 74HC151:
   - Connect selector inputs (C, B, A) to DIP switches.
   - Route MUX inputs to GND, Vcc, or square wave as needed.
3. Debug: Use LED on MUX output and check all 8 combinations.
4. Add NOR gates for enabling/disabling green/red LEDs.
5. Connect MUX output through NOR path to LEDs.
6. Validate output behavior for each sensor combo.

### ⚠️ Notes

- Use `x` (don't care) values in K-maps to simplify logic.
- Treat "F" (flashing) as logic 1 for enable path.
- Double-check Vcc/GND orientation on all ICs.
- Never hot-swap components with battery ON.

---

## ✅ Outcomes

- Correctly interpreted sensor inputs and drove LEDs accordingly.
- Verified LED behavior (ON, OFF, FLASHING) for all valid combinations.
- Practiced logic design with MUX, NOR, and 555-based timing.
