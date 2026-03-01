DR7-Keyboard
A mechanical keyboard build on YD-RP2040 with an OLED display and backlights

Build for MX switches

A sligthly modified 96% keyboard layout with 4 extra keys for managing onboard firmware (103 keys total)

Keyboard CAD assembly

Keyboard layout

Keyboard parts

Why is this one special
It's a keyboard with a customisable OLED that helps to manage, and control parts of the firmware like changing backlighting color, showing typing speed and much more

The firmware is also open-source so anyone can customise and add features to their keyboard

PCB
PCB

Schematic

The keyboard uses a custom PCB with the YD-RP2040 attached to it providing a USB-C connection along with power to the board

The YD-RP2040 is the devboard with a chip running this project. You may be able to use a standard Raspberry PI pico but that was not tested

Case
The keyboard is comprised out of 3 parts. The panel which holds the switches, a back panel and a front panel

Due to their size its impossible to print an entire piece at once, thats why there are sliced versions in the CAD/Sliced folder. You can print them separately and then weld them with a soldering iron together. You should weld the front and the back piece but not the panels as they are held together by the frame anyway

Sliced case

Warning

Due to the size of the keyboard, even the sliced version requires 216 x 139 mm or larger printing plate

Compiling & flashing firmware
Note

You should have CMAKE and GCC installed along with Arm embedded GNU Toolchain arm-none-eabi-gcc

For compilation run the following commands in the project folder: Note that the first command may take a while as it is downloading the SDK from git

cmake -S Firmware -B Firmware/build -G "Ninja"

cmake --build Firmware/build --target Keyboard_Firmware

To load the firmware into the RP2040 chip, press the BOOT button on the YD-RP2040 devboard and plug it into your computer. It should appear as a drive in which you insert the Keyboard_Firmware.uf2 file inside the Firmware/build/ folder. The keyboard should reboot itself and load the active firmware

To reflash the board just repeat the steps above

BOM
Product name	Product description	Product link	Product unit cost inc. Tax (€)	Product amount	Product total cost (€)	Running total (€ with tax and shipping)
YD-RP2040	RPI pico-like microcontroller board	Link	2.99 €	1	2.99 €	2.99 €
74AHCT125DR	Logic level shifter IO	Link	3.01 €	1	3.01 €	6.00 €
100nF 0805 Ceramic Capacitor (>= 6.3V)	Decoupling capacitor	Link	0.02 €	105	1.82 €	7.82 €
10kΩ 0805 Resistor	Pull-up resistor	Link	0.02 €	2	0.04 €	7.85 €
1N4148W Diode	Keyboard matrix diode	Link	0.02 €	103	1.77 €	9.63 €
Kailh Hot-Swap Sockets for Gateron x103	PCB sockets for switches	Link	8.24 €	1	8.24 €	17.87 €
Gateron Switch G Pro 3.0	Mechanical keyboard switches	Link	0.37 €	103	38.11 €	55.98 €
1.5 Inch OLED Display 128x128 I2C	OLED Screen	Link	4.25 €	1	4.25 €	60.23 €
SK6812 Mini RGB LED x200	Backlight LEDs	Link	3.38 €	2	6.76 €	66.99 €
Keycap set	set of keycaps for keyboard	Link	16.93 €	1	16.93 €	83.92 €
M3x8 screws	screws for PCB and case assembly	Link	0.05 €	8	0.40 €	84.32 €
Hot melt inserts MxL4xOD4.2	inserts for case assembly	Link	0.11 €	8	0.88 €	85.20 €
Silicone feet 12x3mm x4	anti-slip feet for case	Link	0.72 €	1	0.72 €	85.92 €
PCB	w/o assembly (estimate)	Link	40.00 €	1	40.00 €	125.92 €
