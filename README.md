# Astable 555 Timer PCB

> Eagle CAD PCB Design | 2-Layer Board | NE555 + 7805

---

## Project Description
A variable-frequency astable oscillator PCB designed in **Eagle CAD** using the classic **NE555 timer IC** in astable mode. A **100kΩ potentiometer** allows real-time frequency adjustment. Input power (+12V) is regulated to +5V using a **7805 linear regulator**. An LED blinks at the output frequency for visual feedback. The board includes a DC barrel jack and a 2-pin power header for flexible power input.

**Short Description (≤350 chars):**
> Astable 555 timer PCB with variable frequency output using 100kΩ potentiometer. NE555 IC generates continuous square wave with LED indicator. 12V input regulated via 7805. Designed in Eagle CAD.

---

## Key Components

| Component | Description |
|-----------|-------------|
| **NE555** | Timer IC in astable (free-running oscillator) mode |
| **7805 (IC1)** | 5V linear voltage regulator (TO-92) |
| **R5 – 100kΩ POT** | Variable resistor for frequency tuning |
| **R1 – 10kΩ** | Timing resistor Ra |
| **R2 – 1kΩ** | Timing resistor Rb |
| **R3 – 330Ω** | LED current limiting resistor |
| **C3, C4 – 10µF** | Timing capacitor and supply filter |
| **C1, C2 – 0.1µF** | Bypass/decoupling capacitors |
| **LED1** | Output frequency visual indicator |
| **DC JACK** | 2.0mm barrel jack for power input |

---

## Design Features
- NE555 wired in astable mode for continuous square wave output
- 100kΩ potentiometer enables real-time frequency adjustment
- Frequency approximately: f = 1.44 / ((R1 + 2×R2 + POT) × C3)
- 12V DC input regulated to stable 5V via 7805 regulator
- LED blinks at oscillator frequency – instant visual verification
- Dual power input: DC barrel jack + 2-pin pin header
- All through-hole components for easy soldering and prototyping

---

## Signal Flow
```
DC Barrel Jack / JP1 Header – 12V Input
       ↓
  7805 – 5V Voltage Regulator
       ↓
  NE555 Timer IC – Astable Mode
       ↑
  R1 (10kΩ) + R2 (1kΩ) + R5 POT (100kΩ) + C3 (10µF) – RC Timing
       ↓
  Square Wave Output (Pin 3)
       ↓
  R3 (330Ω) + LED1 – Visual Output Indicator
```

---

## Files Included
- Astable_555_timer.sch – Eagle Schematic
- Astable_555_timer.brd – Eagle PCB Layout
- GERBER_FILES_Astable_555_timer_2026-05-20.zip – Gerber files

---
