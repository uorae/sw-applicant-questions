## Tinkercad Circuit Link

rachel guo z5479690
https://www.tinkercad.com/things/fv0NEcT9C08-bluesat-sw-app?sharecode=IlD-09bv0A4_ZZRB-3UKaLQFcTMRhPsdSoblFk42bL8

## Program Explanation
This circuit works by sensing the current state of the system in every loop iteration, and adjusting LED behaviour accordingly. 
In the IDLE state, the button is LOW and waits for a button press. In the ARMED state the LED pulses for a randomised interval. In the STARTED state, the button is HIGH and waits for a reaction from the user. In the REACTION state, the LED blinks based on the reaction time. In the F_START state, the LED flashes rapidly for 2 seconds.
In each state, the circuit waits for a button press or the end of an interval timer to transition to another state. 

Assumptions:
 - The system returns to idle following the serial output and LED feedback after a reaction.
 - The system cannot be armed during the LED blink feedback after a reaction or false start.
 - False starts are counted as attempts, but not counted in average reaction time.

Research: This was my first time using Arduino and having any exposure to the hardware side, so I had to research how to get the button and LED working, including the pulse mechanism and the button debouncing, as well as connecting the circuit. 