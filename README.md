## Purpose
Indian houses are built with water tanks to ensure consistent water supply despite municipal inconsistencies or droughts. However, the water tank at my aunt's house is built outside of the house, meaning that it’s inconvenient for my aunt to manually check the water level (and inaccessible, because the tank lid is REALLY heavy). I seek to build a remote water sensor that can detect and transmit the water level conveniently without manual intervention.
## Architecture
Used two ESP-32 microcontrollers, a "sender" and a "receiver". The sender reads distance values from an HC-SR04 ultrasonic sensor, and uses ESP-NOW protocol to transmit to receiver. Receiver interprets sender data - calculates height in a percent - and uploads it to a web server accessible by my aunt.
*NOTE: Much of this code is tutorial code sourced from online and modified to match my needs.*
## Status/Issues
I was able to transmit the data online. Still need to debug the fill ratio calculations and make the webpage dynamic. Also figuring out a long-term power source.
