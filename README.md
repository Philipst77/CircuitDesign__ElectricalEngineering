# Lab 7: Seven Segment Display and BCD Decoder

## 🔍 Objective

This lab explores the functionality and usage of the **5611AH Seven Segment Display (SSEG)** and the **74HC4511 BCD-to-SSEG decoder**. By the end, we demonstrate how to display decimal digits using 4-bit binary-coded decimal inputs.

---

## 🧪 Part A: Manual Control of 5611AH SSEG

### 🔧 Learning Goals

- Understand the pinout and internal structure of the 5611AH SSEG display.
- Light specific segments manually using jumper wires and a current-limiting resistor.

### 🧱 Components

- 5611AH Seven Segment Display (Common Cathode)
- 47Ω resistor (shared across all segments)
- Jumper wires
- Breadboard
- Power supply

### 📐 Segment Layout

- 8 internal LEDs: Segments A-G and decimal point (DP).
- Common Cathode Configuration:
  - CC pins go to GND via the 47Ω resistor.
  - Desired segments are connected to Vcc using jumper wires.

### ⚙️ Implementation Steps

1. Plug the 5611AH display into the breadboard.
2. Connect either of the CC pins to GND via a 47Ω resistor.
3. Light up desired segments by connecting their corresponding pins to Vcc.
4. Demonstrate at least **four numbers** by manually lighting segments and taking photos.

---

## 🔩 Part B: Automatic Display with 74HC4511

### 🔧 Learning Goals

- Interface the 74HC4511 decoder with the SSEG.
- Use DIP switches to input 4-bit BCD numbers (0000 to 1001).
- Display digits 0–9 automatically on the SSEG.

### 🧱 Components

- 5611AH SSEG display
- 74HC4511 BCD-to-SSEG Decoder
- DIP4 switch + pull-up resistors
- 47Ω resistor
- Jumper wires
- Breadboard and power supply

### 📐 Pin Configuration

- **BCD Input Pins**: D3 (Pin6), D2 (Pin2), D1 (Pin1), D0 (Pin7)
- **Segment Output Pins**: a-g → Pins 13, 12, 11, 10, 9, 15, 14
- **Control Pins**:
  - LT (Pin3) → Vcc
  - BL (Pin4) → Vcc
  - LE (Pin5) → GND
- Power: Vcc (Pin16), GND (Pin8)

### ⚙️ Implementation Steps

1. Connect control pins as described to disable test, blanking, and latching.
2. Use DIP switches to send 4-bit BCD inputs to D3–D0.
3. Connect segment output pins (a–g) from the 74HC4511 to matching pins on the SSEG.
4. Leave the 47Ω resistor connected between CC pin and GND.
5. Test all inputs from `0000` to `1001` (0–9) and ensure each digit appears correctly on the display.
6. Take photos for each digit.

### ⚠️ Notes

- **BCD values from 1010 to 1111 (10–15)** will not produce output on the SSEG.
- Ensure correct Vcc/GND orientation on the decoder IC — **reversing will damage the chip!**
- Use color-coded long jumper wires to reduce wiring confusion.

---

## ✅ Outcomes

- Successfully displayed digits 0–9 using a BCD input and decoder IC.
- Gained hands-on understanding of SSEG pin mapping and decoder IC behavior.
- Reinforced prototyping skills and use of control signals in digital logic.
