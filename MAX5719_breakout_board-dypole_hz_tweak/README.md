Teensy + MAX5719 high-resolution (low-speed) DAC.

Interface is via SPI, all microcontroller signals are isolated using MAX14850ASE (or compatible) capacitive isolator. A galvanically isolated power supply may be used to provide the +/-15V DAC/analog buffer supply, so microcontroller USB does not need to be isolated.
Tested up to 20MHz SPI on a breadboard, good layout of microcontroller to breakout board PCB may allow for higher speeds (MAX5719 is specified up to 50MHz).

Onboard 5 V voltage reference, output is then scaled up by 2 for a 10V range.
