# Lab 12: FSM with JK Flip-Flops (T and SR Configurations)

## 🔍 Objective

This lab builds a **4-state finite state machine (FSM)** using **74HC109 JK flip-flop ICs** configured as both **T flip-flops** and **SR latches**. The FSM controls two LEDs based on button input and features “sticky” state memory. A **555 timer** serves as the clock source.

---

## 🧪 FSM Design and Construction

### 🔧 Learning Goals

- Configure JK flip-flops as T flip-flops and SR latches.
- Use T flip-flops to toggle LED output based on a square wave clock.
- Use SR latches to asynchronously enable/disable toggling.
- Implement FSM states controlled by button input.
- Understand sticky behavior and reset logic.

### 🧱 Components

- 2 × 74HC109 JK Flip-Flop ICs (dual flip-flops)
- LMC555 Timer IC (clock generator)
- 3 × SPST Push buttons (A, B, RST)
- Red LED (T flip-flop A output)
- Green LED (T flip-flop B output)
- Yellow LED (clock debug)
- 330Ω resistors
- 10kΩ resistors
- 1MΩ trimpot
- 1 × 1µF capacitor
- Breadboard, jumper wires
- 3V battery pack

### 🧠 FSM Behavior Table

| RST | A | B | State | Description                          |
|-----|---|---|--------|--------------------------------------|
| ✔   |   |   | S1     | Both LEDs OFF                        |
|     | ✔ |   | S2     | Red LED flashes                      |
|     |   | ✔ | S3     | Green LED flashes                    |
|     | ✔ | ✔ | S4     | Both LEDs flash                      |

- “Sticky” behavior: LEDs stay flashing until reset.
- RST clears both SR latches and disables toggling.
- A and B buttons independently SET their respective latches.

### ⚙️ Implementation Steps

1. Build square wave clock using 555 timer and verify with yellow LED.
2. Configure two JK flip-flops as **T flip-flops**:
   - J = Vcc, K = GND, PRE = Vcc, CLK = from 555, CLR = from SR latch Q.
3. Configure the other two JK flip-flops as **SR latches**:
   - J = Vcc, K = GND, PRE = SET input, CLR = RST input, CLK = GND.
4. Connect button A to red SR latch SET, button B to green SR latch SET.
5. Connect common RST button to both SR latch CLR inputs.
6. Wire T flip-flop outputs to red and green LEDs.
7. Test FSM transitions per truth table above.

### ⚠️ Notes

- No debouncing needed — latches retain SET/RESET even with bouncing.
- Clock is always running; toggling only occurs if SR latch output is high.
- T flip-flops toggle output on each rising clock edge when enabled.

---

## ✅ Outcomes

- Successfully built and demonstrated a **4-state FSM**.
- Verified sticky LED toggling via SR-controlled T flip-flops.
- Demonstrated full state transitions using button inputs and reset.
- Confirmed correct timing behavior via yellow LED (square wave debug).
