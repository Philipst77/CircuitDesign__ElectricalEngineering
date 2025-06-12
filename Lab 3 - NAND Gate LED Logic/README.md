# Lab 3: Switch and Button Controlled LED Circuit 💡🔘

## Overview

This lab involves building a digital logic circuit using three LEDs where:

- 🔴 The red LED is **always ON**
- 🟢 The green LED is controlled by a **push button**
- 🟡 The yellow LED is controlled by a **DIP switch**

The main goal is to understand the operation of buttons and DIP switches, and how they serve as logical input devices in a circuit. You'll also gain practical breadboarding experience with both flexible and rigid components.

---

## Objectives

- Build a logic circuit using three LEDs, resistors, a DIP switch, and a button
- Learn how push buttons (SPST switches) and DIP switches work in a circuit
- Understand breadboard mechanics, especially for rigid components

---

## Components Used

- 3x 330Ω resistors
- 3x LEDs (red, green, yellow)
- 1x SPST push button
- 1x DIP4 switch (only 1 of 4 switches used)
- Jumper wires
- Breadboard
- 3V power supply

---

## Circuit Description

- **Red LED**: Connected directly to power and ground via a resistor. Always ON.
- **Green LED**: Wired through the push button. Turns ON only when the button is pressed.
- **Yellow LED**: Controlled by the DIP switch (SW1). Turns ON when the switch is flipped ON.

---

## Button Behavior 🔘

The push button (SPST):

- OFF by default
- Connects (1)-(2) to (3)-(4) when pressed
- Allows dynamic control of the green LED when wired into the circuit

Wiring Strategy:
- (1)-(2) pair connected to one side of the breadboard and tied to Vcc
- (3)-(4) pair connected to a resistor and then to the green LED

---

## DIP Switch Behavior ⚙️

The DIP4 switch:

- Only **SW1** is used in this lab
- ON connects the top and bottom pins (shorts them)
- OFF disconnects them

Wiring Strategy:
- Top row of SW1 connects to the yellow LED through a resistor
- Bottom row connects to Vcc

---

## Breadboard Insights

- Rigid components like buttons and DIP switches follow standard 0.1" pin spacing
- DIP and button devices span the center gutter of the breadboard (0.3" across)
- Be mindful of body placement: some rows become unusable due to physical obstruction

---

## Functionality Demo 🎬

| Component        | Initial State | Interaction           | Result               |
|------------------|---------------|------------------------|-----------------------|
| Red LED          | ON            | Static                 | Always lit 🔴        |
| Green LED        | OFF           | Press button           | Turns ON while pressed 🟢 |
| Yellow LED       | OFF           | Flip DIP switch ON     | Turns ON 🟡           |

---

## Summary

This lab demonstrated:

- How to control circuit outputs using input components (button, switch)
- Breadboarding techniques for rigid and flexible parts
- Foundational knowledge to build more complex logic circuits in upcoming labs

> ✅ Don't forget to disconnect the power when you're done!

---
