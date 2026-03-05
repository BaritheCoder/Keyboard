# 1800 Compact Keyboard

A custom mechanical keyboard built around the **YD-RP2040** microcontroller, featuring an **OLED display**, **rotary encoder**, and **RGB backlighting** — all designed for MX switches.

The layout is a modified **1800 compact** with **96 keys** total. The firmware is fully open-source, so feel free to dig in and make it your own.

---

## What's the idea?

The OLED screen is the main thing that sets this apart — it can show stuff like:

- Volume level
- Typing speed (WPM)
- System info
- Whatever else you want to add

Since the firmware is open-source, anyone can extend it and add new features without too much hassle.

---

## PCB

> PCB renders/screenshots coming soon.

| PCB | Schematic |
|:---:|:---:|
| ![PCB](https://github.com/user-attachments/assets/6a6a1147-d90b-47d4-9a4e-4a0a254ca019) | ![Schematic](https://github.com/BaritheCoder/Keyboard/blob/main/Images/Screenshot%202026-02-20%20193307.png?raw=true) |

## Case

The case is split into **3 parts**:

- Frame
- Back panel
- Front panel

| ![PCB](https://github.com/user-attachments/assets/6a6a1147-d90b-47d4-9a4e-4a0a254ca019) | ![Schematic](https://github.com/BaritheCoder/Keyboard/blob/main/Images/Screenshot%202026-02-20%20193307.png?raw=true) |


## Bill of Materials

| Product | Description | Link | Unit Cost (€ inc. Tax) | Qty | Total (€) | Running Total (€) |
|---|---|---|---:|---:|---:|---:|
| YD-RP2040 | Raspberry Pico-like MCU | [Link](#) | 1.42 | 1 | 1.42 | 1.42 |
| 74AHCT125 | Logic level shifter | [Link](#) | 2.95 | 1 | 2.95 | 4.37 |
| 0.1µF 0805 SMD Capacitor x100 | Decoupling caps | [Link](#) | 0.0161 | 100 | 1.61 | 5.98 |
| 470µF Bulk Capacitor 7343 | Bulk caps | [Link](#) | 0.788 | 5 | 3.94 | 9.92 |
| 4.7kΩ 0805 Resistor | Pull-up resistor | [Link](#) | 4.10 | 1 | 4.10 | 14.02 |
| 330Ω 0805 Resistor | Voltage regulator resistor | [Link](#) | — | — | 0.00 | 14.02 |
| SOD-123 Diode | Matrix diodes | [Link](#) | 0.0183 | 100 | 1.83 | 15.85 |
| SK6812 Mini RGB LEDs x100 | Per-key RGB | [Link](#) | 0.0365 | 100 | 3.65 | 19.50 |
| EC11 Rotary Encoder | Volume/function knob | [Link](#) | 1.285 | 2 | 2.57 | 22.07 |
| Rotary Encoder Knob | Knob cap | [Link](#) | 0.675 | 2 | 1.35 | 23.42 |
| Gateron Jupiter Banana | Switches | [Link](#) | 0.28 | 110 | 30.80 | 54.22 |
| Gateron Hot-Swap Sockets x110 | Switch sockets | [Link](#) | 0.10 | 110 | 11.00 | 65.22 |
| Silicone Feet 12x3 | Bottom case feet | [Link](#) | 0.2075 | 4 | 0.83 | 66.05 |
| M3x8 Screws | Case assembly | [Link](#) | 2.28 | 4 | 2.28 | 68.33 |
| Hot Melt Inserts M3xL4xOD4.2 | Case assembly | [Link](#) | 0.0973 | 30 | 2.92 | 71.25 |
| 0.91" OLED Display 128x32 | Screen | [Link](#) | 1.96 | 1 | 1.96 | 73.21 |
| PCB | Main board | [Link](#) | 40.00 | 1 | 40.00 | 113.21 |
| Keycap Set | Keycaps (133 keys) | [Link](#) | 0.142 | 133 | 18.82 | 132.03 |

### 💰 Estimated Total: ~ €132 (~ $143 USD)

---

## Firmware

Firmware documentation and build instructions will be added once the keyboard is fully assembled and the code has been tested on real hardware. No point documenting something that hasn't been verified yet.
