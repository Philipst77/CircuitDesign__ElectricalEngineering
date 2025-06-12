# 🔁 Lab 4: 555 Timer – Square Wave Generator

## 🧠 Objective

This lab focuses on using a 555 Timer Integrated Circuit (IC) in astable mode to generate a continuous square wave. Through hands-on circuit construction and observation, the goal is to:
- Understand how a 555 Timer operates in multivibrator mode
- Use passive components (resistors, capacitor, trimpot) to control oscillation frequency
- Alternate two LEDs using the timer’s output
- Read and follow datasheets for correct IC pinout configuration

---

## 🧰 Components

- 1 × LMC555 Timer IC (DIP-8)
- 1 × Red LED  
- 1 × Green LED  
- 2 × 330Ω resistors (for LEDs)  
- 1 × 10kΩ resistor  
- 1 × 1MΩ trimpot  
- 1 × 1µF capacitor  
- 1 × 3V battery and battery holder  
- Breadboard and jumper wires  

---

## 🧪 Procedure

1. **IC Setup:**
   - Place the LMC555 IC across the centerline of the breadboard.
   - Connect Vcc (Pin 8) to the positive rail and GND (Pin 1) to the ground rail.

2. **Component Wiring:**
   - Use the trimpot and 10kΩ resistor in series between pins 7 (Discharge) and 8 (Vcc).
   - Connect a 1µF capacitor between pin 6 (Threshold) and GND.
   - Join pins 2 (Trigger) and 6 together.
   - Tie pin 4 (Reset) to Vcc.
   - Connect the output (pin 3) to both LEDs via separate 330Ω resistors — one LED to GND, the other to Vcc.

3. **Power On:**
   - Attach the battery to power the circuit.
   - Adjust the trimpot to vary the blink rate of the LEDs.

---

## 🔎 Observations

- The LEDs flash alternately, confirming the square wave output from the 555 Timer.
- The frequency of blinking depends on the RC time constant, which is adjustable via the trimpot.
- The circuit demonstrates fundamental principles of timing, digital switching, and pulse generation.

---

## 📸 Demonstration

> ✅ A video or photo showing alternating LED blinking should be included in this directory.

---

## 💡 Key Concepts

- **Astable Mode:** The 555 timer continuously oscillates without external triggering.
- **RC Timing:** The resistor-capacitor combination determines the frequency of the output.
- **Practical Use:** This type of circuit is foundational for clocks, timers, and digital pulse generators.

---

## ✅ Outcome

- Successfully built and tested a square wave generator using a 555 Timer.
- Verified functionality through LED flashing.
- Developed familiarity with IC datasheets, pin mapping, and analog timing elements.

