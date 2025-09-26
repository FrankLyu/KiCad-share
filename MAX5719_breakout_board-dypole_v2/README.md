Teensy MAX5719 high-resolution (low-speed) AWG v2 in dypole. Problems are at the bottom of the file.

Interface is via SPI, all microcontroller signals are isolated using MAX14850ASE (or compatible) capacitive isolator. A galvanically isolated power supply may be used to provide the +/-15V DAC/analog buffer supply, so microcontroller USB does not need to be isolated. Tested up to 20MHz SPI on a breadboard, good layout of microcontroller to breakout board PCB may allow for higher speeds (MAX5719 is specified up to 50MHz).

Onboard 5 V voltage reference, output is then scaled up by 2.0x for a 10V range.

JP1 is for unipolar output. JP2/3 for bipolar.

We chose Op Amp OP2192. Voltage reference chip MAX6126 (which has a demo schematic for MAX5719). The exact voltages on board should be +12, -12 and +5.376 V.

GPT says we should power the dirty MAX14850 with another power rail. Is it necessary?
