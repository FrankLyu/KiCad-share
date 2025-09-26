Breakout board for the MAX5719 high-resolution (low-speed) DAC.

Interface is via SPI, all microcontroller signals are isolated using MAX14850ASE (or compatible) capacitive isolator. A galvanically isolated power supply may be used to provide the +/-15V DAC/analog buffer supply, so microcontroller USB does not need to be isolated.
Tested up to 20MHz SPI on a breadboard, good layout of microcontroller to breakout board PCB may allow for higher speeds (MAX5719 is specified up to 50MHz).

Onboard 4.096V voltage reference, output is then scaled up by 2.5x for a 10V range.

The circuit is very similar to the MAX5719BOB, except for the factor of 2.5x scaling and removal of negative voltage capabilities. That circuit also suffered from non-linearities above 3.3V, which this design resolves.
