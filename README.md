# peltier-vaccine-carrier
Portable vaccine carrier using Peltier module for 2-8°C cold chain
Portable Vaccine Carrier with ON/OFF Peltier Temperature Control

A real-time temperature stabilisation system for portable vaccine storage. An Arduino Uno reads the interior temperature of an insulated carrier through a DS18B20 sensor and switches a TEC1-12706 Peltier module on and off through an IRLZ44N MOSFET to hold a user-defined setpoint between 2 °C and 8 °C.

1.The DS18B20 continuously measures the interior temperature and sends it to the Arduino.
2.The Arduino computes the error between the measured temperature and the user-defined setpoint.
3.Based on the error, the controller switches the IRLZ44N MOSFET, which drives the TEC1-12706 Peltier module.
4.The loop repeats continuously, so the internal temperature is corrected even when the outside conditions change.

The IRLZ44N MOSFET acts as an electronic switch between the Arduino and the Peltier. The Arduino's 5 V signal turns it fully on, letting up to 6 A flow with about a 0.15 V drop and under 1 W loss. When the setpoint is reached, the signal goes low and the Peltier stops.
