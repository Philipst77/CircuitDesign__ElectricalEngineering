# Digital Logic Lab – Picnic Decision Circuit 🚦🌤️🧺

## Overview

This lab explores how to use **Boolean algebra**, **De Morgan's laws**, and **Karnaugh maps (K-maps)** to build a decision-making digital logic circuit using two new ICs:

- `74HC02`: Quad NOR gate
- `74HC04`: Hex inverter

### Objective
Design a circuit to determine whether **Gina** goes to a family picnic based on:
- Alice's decision (A)
- Bob's decision (B)
- Whether it is sunny (S)

Output:
- `G = 1` ➝ Gina goes to the picnic
- `G = 0` ➝ Gina stays home

## Logical Conditions

Gina’s decision depends on two conditions:

1. **Sunny + at least one person going**:  
   If `S = 1` and `(A or B) = 1`, then `G = 1`

2. **Not sunny + both going**:  
   If `S = 0` and `(A and B) = 1`, then `G = 1`

This requires:
- 4 NOR gates (from `74HC02`)
- 4 inverters (from `74HC04`)

## Hardware Components 🧩

- `74HC02` (Quad NOR): 4 gates
- `74HC04` (Hex Inverter): 4 gates used
- DIP Switches: Inputs A, B, and S
- LEDs:
  - Green LED → Gina goes (G = 1)
  - Red LED → Gina stays (G = 0)
- Resistors (typically 330Ω for LEDs)
- Breadboard & jumper wires
- Battery pack

## Circuit Behavior 🚨

- Output of final NOR gate is inverted to drive LEDs.
- Pinouts from IC datasheets were carefully selected to reduce wire length and crossing.
- Uses both long jumper wires and short pre-cut jumpers.

## Prototype Testing ✅

You should test all 8 combinations of inputs (A, B, S). Example:

- **A=1, B=1, S=1** ➝ G = 1 → Green ON, Red OFF
- **A=0, B=0, S=1** ➝ G = 0 → Red ON, Green OFF

💡 **Reminder:** Turn OFF your battery pack after testing!

## Summary 🧠

This lab demonstrated how real-life decision logic can be translated into digital circuits. Through simplification and IC selection, a logical function was optimized and implemented effectively on a breadboard.

---

