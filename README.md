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

## Compiling & flashing firmware

> ℹ️ **Note**  
> You should have **CMAKE** and **GCC** installed along with Arm embedded GNU Toolchain `arm-none-eabi-gcc`

For compilation run the following commands in the project folder:  
Note that the first command may take a while as it is downloading the SDK from git.

```bash
cmake -S Firmware -B Firmware/build -G "Ninja"
cmake --build Firmware/build --target Keyboard_Firmware
