# 1800 compact keyboard

A mechanical keyboard build with the **YD-RP2040** Pico like microcontroller with an **OLED display**, **Rotary encoder** for basic functions and **backlights**.

Build for **MX switches**.

A modified **1800 layout** with **96 total keys**  and a rotary encoderfor managing onboard firmware (**___ keys total**).

---

## What is it?

It’s a keyboard with a customizable **OLED** that helps manage and control parts of the firmware like:
- changing backlighting color
- showing typing speed
- system/status info
- and much more

The firmware is also **open-source**, so anyone can customize and add features to the keyboard.

---

## PCB

> Put PCB renders/screenshots here.

![PCB](docs/images/pcb.png)

### Notes
- Controller: **YD-RP2040**
- You may be able to use a standard **Raspberry Pi Pico** (not tested)
- Hot-swap: Yes/No
- RGB LEDs: SK6812/WS2812 (___ pcs)
- OLED: I2C (___)

---

## Case

The keyboard is comprised out of **3 parts**:
- The panel which holds the switches
- A back panel
- A front panel

Due to the size it’s impossible to print an entire piece at once, that’s why there are sliced versions in the  
`CAD/Sliced` folder.

You can print them separately and then weld them together with a soldering iron.  
You should weld the **front** and the **back** piece but **not** the panels as they are held together by the frame anyway.

![Case exploded](docs/images/case_exploded.png)

> ⚠️ **Warning**  
> Due to the size of the keyboard, even the sliced version requires **___ x ___ mm** or larger printing plate.

---

| Product name | Product description | Product link | Product unit cost inc. Tax (€) | Product amount | Product total cost (€) | Running total (€ with tax and shipping) |
|---|---|---|---:|---:|---:|---:|
| YD-RP2040 | Raspbery Pico like microcntroller board | [Link](#) | 1.42 | 1 | 1.42 | 1.42 |
| 74AHCT125 | Logic level shifter | [Link](#) | 2.95 | 1 | 2.95 | 4.37 |
| 0.1µF 0805 SMD Capacitor x100 | Decoupling capacitors | [Link](#) | 0.0161 | 100 | 1.61 | 5.98 |
| 470µF Bulk Capacitor 7343 | Bulk capacitors | [Link](#) | 0.788 | 5 | 3.94 | 9.92 |
| 4.7kΩ 0805 Resistor | Pull-up resistor | [Link](#) | 4.10 | 1 | 4.10 | 14.02 |
| SOD-123 Diode | Keyboard matrix diode | [Link](#) | 0.0183 | 100 | 1.83 | 15.85 |
| SK6812 Mini RGB LEDs x100 | Keyswitch LEDs | [Link](#) | 0.0365 | 100 | 3.65 | 19.50 |
| EC11 Rotary Encoder | The twisty thing on the top right | [Link](#) | 1.285 | 2 | 2.57 | 22.07 |
| Rotary Encoder Knob | Knob for the rotary encoder | [Link](#) | 0.675 | 2 | 1.35 | 23.42 |
| Gateron Jupiter Banana | Creamy mechanical switches | [Link](#) | 0.28 | 110 | 30.80 | 54.22 |
| Gateron Hot-Swap Sockets x110 | PCB sockets for switches | [Link](#) | 0.10 | 110 | 11.00 | 65.22 |
| Silicone Feet 12x3 | Anti-slip feet for bottom of case | [Link](#) | 0.2075 | 4 | 0.83 | 66.05 |
| M3x8 Screws | For case assembly | [Link](#) | 2.28 | 4 | 2.28 | 68.33 |
| Hot Melt Inserts M3xL4xOD4.2 | For case assembly | [Link](#) | 0.0973 | 30 | 2.92 | 71.25 |
| 0.91" OLED Display 128x32 White | For testing and shortcuts | [Link](#) | 1.96 | 1 | 1.96 | 73.21 |
| PCB | The main board | [Link](#) | 40.00 | 1 | 40.00 | 113.21 |

---

### 💰 Estimated Total Cost


## Compiling & flashing firmware

> ℹ️ **Note**  
> You should have **CMAKE** and **GCC** installed along with Arm embedded GNU Toolchain `arm-none-eabi-gcc`

For compilation run the following commands in the project folder:  
Note that the first command may take a while as it is downloading the SDK from git.

```bash
cmake -S Firmware -B Firmware/build -G "Ninja"
cmake --build Firmware/build --target Keyboard_Firmware
