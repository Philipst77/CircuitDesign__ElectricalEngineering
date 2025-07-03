# Lab 8: 4-Bit Full Adder with Decimal Display

## 🔍 Objective

This lab demonstrates how to build a modular digital system using a **74HC283 4-bit full adder** to add two 4-bit binary numbers and display the result on a **5611AH Seven Segment Display (SSEG)** via a **74HC5411 BCD decoder**. It introduces the concept of **modular design** and **data buses** in circuit schematics.

---

## 🧪 Part A: Modular Adder Circuit with Carry Handling

### 🔧 Learning Goals

- Understand the pinout and operation of the 74HC283 4-bit full adder.
- Apply modular design by reusing the DIP switch and BCD display subcircuits.
- Inject binary values using DIP switches and a Carry In push button.
- Display valid decimal sums (0–9) using the BCD decoder and SSEG.
- Use an LED to indicate Carry Out from the adder when overflow occurs.

### 🧱 Components

- 74HC283 (4-bit binary adder)
- 74HC5411 (BCD to 7-segment decoder)
- 5611AH Seven Segment Display (SSEG)
- 2 × DIP4 switches (Inputs A and B)
- SPST push button (Carry In)
- Yellow LED (Carry Out indicator)
- 9 × 10kΩ resistors (pull-ups)
- 1 × 47Ω resistor (common cathode resistor)
- 1 × 330Ω resistor (for LED)
- Breadboard, jumper wires
- 3V battery pack

### 📐 Pin Summary

- **Input A**: A3 (Pin12), A2 (Pin14), A1 (Pin3), A0 (Pin5)
- **Input B**: B3 (Pin11), B2 (Pin15), B1 (Pin2), B0 (Pin6)
- **Carry In**: Cin (Pin7) — active low via push button
- **Sum Output**: S3 (Pin10), S2 (Pin13), S1 (Pin1), S0 (Pin4)
- **Carry Out**: Cout (Pin9) — connected to Yellow LED

### ⚙️ Implementation Steps

1. Build the **BCD display module** (74HC5411 + 5611AH) from the previous lab.
2. Wire DIP switches A and B with pull-up resistors and connect them to 74HC283 input pins.
3. Connect the push button to 74HC283’s Cin pin for manual Carry In control.
4. Route the 4-bit sum output from 74HC283 to the BCD decoder input.
5. Connect Cout pin to the yellow LED through a 330Ω resistor.
6. Power all ICs carefully — verify Vcc and GND connections.

### ⚠️ Notes

- Cin is **active low**: Pressing the button sets Cin = 0.
- Cout = 1 lights up the yellow LED to indicate overflow beyond 4 bits.
- The BCD decoder only displays sums 0–9. Invalid BCD values (10–15) result in a blank display.
- Sums > 15 are interpreted as `sum % 16`, which may display a valid digit depending on the lower nibble.

---

## ✅ Outcomes

- Built a modular 4-bit adder system with BCD display.
- Understood how to interpret carry logic using LED feedback.
- Gained experience in designing reusable circuit modules and using data buses to simplify schematics.
