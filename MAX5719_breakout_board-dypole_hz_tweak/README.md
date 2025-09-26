Teensy MAX5719 high-resolution (low-speed) AWG v1 in dypole. Problems are at the bottom of the file.

Interface is via SPI, all microcontroller signals are isolated using MAX14850ASE (or compatible) capacitive isolator. A galvanically isolated power supply may be used to provide the +/-15V DAC/analog buffer supply, so microcontroller USB does not need to be isolated.
Tested up to 20MHz SPI on a breadboard, good layout of microcontroller to breakout board PCB may allow for higher speeds (MAX5719 is specified up to 50MHz).

Onboard 5 V voltage reference, output is then scaled up by 2.0x for a 10V range.

JP1 is for unipolar output. JP2/3 for bipolar.

We chose Op Amp OP2192. Voltage reference chip MAX6126 (which has a demo schematic for MAX5719). The exact voltages on board should be +13.2, -13.2 and +5.376 V.

Production (purchased at JLCPCB) on Sep 9th 2025. This version has 3 problems. 

First, the zero resistors are not soldered. The voltage divider for ADP7118 5 V is wrong.

Second, the +13.2 V and -13.2 V fight each other. Negative prevents positive voltage from turning on. This might be the safe feature of ADP7118. After taking away the OP2192, the problem is gone.

Third, the BNC connector is not well shielded, and it picks up high frequency (>10 MHz RF) from the air.

To address the second problem, we go back to LM7812, LM7912 to power the Op amp. It doesn't affect the noise performance.
