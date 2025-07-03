# Lab 11: 4-bit Shift Register with JK Flip-Flops

## 🔍 Objective

This lab creates a **4-bit shift register** using two **74HC109 JK flip-flop ICs** configured as D flip-flops. A **555 timer** serves as the clock, and a button-injected input bit propagates through the flip-flops.

---

## 🧪 Part A: Shift Register Construction

### 🔧 Learning Goals

- Configure JK flip-flops as D flip-flops.
- Chain 4 D flip-flops into a shift register.
- Use an RC debouncer to clean push button input.
- Inject and observe bit trains shifting over time.

### 🧱 Components

- 2 × 74HC109 JK Flip-Flop ICs
- LMC555 Timer IC
- 2 × SPST Push buttons (In, RST)
- 4 Red LEDs (bit output)
- Yellow LED (clock debug)
- 330Ω resistors
- 10kΩ resistors
- 1MΩ trimpot
- 2 × 1µF capacitors (for debounce)
- Breadboard, jumper wires
- 3V battery pack

### 📐 Shift Register Behavior

- Injected bit shifts right on every rising clock edge.
- Reset button clears all flip-flops (0000).
- In button (debounced) injects “1” into leftmost flip-flop.

### ⚙️ Implementation Steps

1. Build and test 555 square wave generator.
2. Connect 74HC109 pins to configure JK as D flip-flops.
3. Wire all CLR pins to a common RST push button.
4. Create debounce circuit for In button using RC pair.
5. Use Q outputs to drive red LEDs for bit visualization.
6. Inject sequences like:
   - `0000 → 1000 → 0100 → 0010 → 0001 → 0000`
   - `0000 → 1000 → 1100 → 0110 → 0011 → 0001 → 0000`

### ⚠️ Notes

- PRE unused (tied to Vcc), CLR used for reset.
- Clock drives all 4 flip-flops simultaneously.
- In button must be held long enough to coincide with clock rising edge.

---

## ✅ Outcomes

- Built and tested a fully functional 4-bit shift register.
- Verified injection and movement of 1s across flip-flops.
- Demonstrated debounce circuit and synchronized timing.
