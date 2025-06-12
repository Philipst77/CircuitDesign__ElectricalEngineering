# 🔌 Lab 5: NAND Gate Logic and Prototyping with 74HC00

## 🧠 Learning Objectives

- Understand the Boolean behavior of NAND gates.
- Build circuits to demonstrate NAND functionality and inversion.
- Use pull-up resistors and DIP switches to apply logic values.
- Learn practical chip wiring using the 74HC00 quad NAND gate IC.

## ⚙️ Components Used

- 74HC00 IC (contains 4 NAND gates)
- 2 × 330Ω resistors (for LEDs)
- 2 × 10kΩ resistors (pull-up resistors)
- Red LED (for Z output)
- Green LED (for Y output)
- DIP4 switch (SW1 and SW2 used)
- 3V battery pack
- Breadboard and jumper wires

## 📐 Circuit Design Overview

This lab demonstrates the NAND gate in two key roles:

1. **Standard NAND gate**: Implements `Y = NOT(A AND B)` using inputs A and B.
2. **Inverter using NAND**: Implements `Z = NOT(Y)` by tying both inputs of the NAND gate to Y.

By combining the two, we effectively show:
- `Y = A ⋅ B` (NAND1 output)
- `Z = NOT(Y)` (NAND2 output)

These outputs are visualized using green and red LEDs respectively.

## 🛠️ Pull-Up Resistor Concept

To assign logic values:
- Switch OFF: Pull-up resistor connects input to Vcc → Logic 1
- Switch ON: Connects input directly to GND → Logic 0

Pull-up resistors are essential; without them, inputs could float and cause unreliable behavior.

## 🔁 DIP Switch and Gate Wiring

- SW1 and SW2 control inputs A and B.
- Inputs connect to 74HC00 Pins 1 and 2.
- NAND1 Output (Y) → Pin 3
- Y is connected to both inputs of NAND2 (Pins 4 and 5)
- NAND2 Output (Z) → Pin 6

**Power Pins:**
- Vcc = Pin 14
- GND = Pin 7  
⚠️ Reversing Vcc and GND can permanently damage the IC.

## 💡 LED Configuration

- Green LED shows output Y (Pin 3 → 330Ω → Green LED → GND)
- Red LED shows output Z (Pin 6 → 330Ω → Red LED → GND)

## 🔬 Testing the Circuit

Test all combinations of inputs:
| A (SW1) | B (SW2) | Y Output | Z Output | Green LED | Red LED |
|--------|---------|----------|----------|------------|---------|
| OFF    | OFF     | 0        | 1        | OFF        | ON      |
| OFF    | ON      | 1        | 0        | ON         | OFF     |
| ON     | OFF     | 1        | 0        | ON         | OFF     |
| ON     | ON      | 1        | 0        | ON         | OFF     |

- **OFF** = Logic 1
- **ON** = Logic 0

## 🧪 Breadboard Prototyping Notes

- Place 74HC00 in center of breadboard, straddling the middle gap.
- Align DIP4 switch and LEDs logically to reduce jumper clutter.
- Use color-coded jumpers to distinguish GND, Vcc, and signals.

## ✅ Summary

This lab demonstrates foundational digital logic concepts using real components:
- How NAND gates can act as universal gates
- Importance of pull-up resistors for stable input logic levels
- Visual verification of logic states via LEDs

🔋 **Always remember to power off the battery pack after the lab is complete.**
