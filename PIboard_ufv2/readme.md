The hopefully final design works. With everything unchanged, the bandwidth is a bit low, only 2.5 kHz for full integral.

Now I changed the resistor for AD8429 to 680 Ohm, so the BW is now 5 kHz. (With default, it is 1.5kOhm, probably too large)

The test sequence:
First change TP-1H to very high, and change TP-1L to very low. Then with 50 Ohm ended on setpoint, another arm with controllable input:
	1. Check on TP4 the diff amp works.
	2. Short J12, check pure P works at TP5.
	3. Short J4, disconnect J12. It is a pure I. check it locks to itself.
	4. Solder bourns 1,2,3 pin to down, middle, and up pins.
	5. Change R32 to 10k if you want the manual out to start from 0 V, instead of some negative value.
	
Simple and nice!

There is a bug. The input signalIn and Setpoint are connected. When locked, SP is high but RF switch is overridden, then SignalIn (measurement) will be a non-zero value! When not locked, SP is low and manual out is high s.t. signalin is high, the measurement may be trimmed by the low SP. 
It can go to at most 4 V. However, if the SP is floating it will be okay?

Next version, we can Change R32 to a place where it is easier to resolder. It sets the lower limit of the manual output.
