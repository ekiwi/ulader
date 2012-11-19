# uLader #

This project aims at creating a backup battery powered bike
lighting system.
It borrows from the great work done by the developers of the
Forumslader and acknowledges this by incorporation
Lader (german for charger) into its name.
The u stands for the micro controller used in this design,
the use of which is going to add a lot more flexibility.

## Component Overview ##

The uLader system consists of these components:
* Main Board: atmega88 uC, ac to dc circuit, charging circuit, 
control switches
* Tail Light: red low power led (dimmable), photo transistor
* Front Light: attiny uC, white low power DLR (dimmabel), white 3W led 
(dimmable), photo transistor
* 2x Rotation Sensor: front and back

## Optional/Future Features ##
* White LED(s) underneath the saddle that can be turned on to find your locks
keyhole
* Pressure Sensor underneath/in the saddle to detect if someone is riding the
bike
* Turn signals on front and back

### Main Board ###

The main board contains the circuit that converts the power from the bike
dynamo, which acts approximately like an AC current source, to about 12V DC.
This circuit is heavily based on the awesome work done by the people behind
the [Forumslader project](forumslader.de).
This circuit is also responsible for charging the LiFePo4 accumulators used.
Check out [forumnslader.de]
(http://www.forumslader.de/Akkus-fuer-12V-Lader.189.0.html) if you want to use
different batteries.

The micro controller part of the Main Board features an atmega88. It was choosen,
because of its ease of use, its low power consumption and because if the number
of pins available.
The atmega is used for the following:
* power mangagement
    * check charging status
    * (indicate status??)
    * cut of power to all devices when battery cells run low
* lighting control
    * measure light intensity
    * measure speed
    * control which lights need to be on and how bright they need to be
    * in auto mode decide when to turn on which lights and auto dim

### Tail Light ####

The Tail Light needs to ensure visibility during the night (and day) from the 
back as well as from the side. In addition to that it must not blind other 
people.  
The CAT4201 led step down driver is used in combination with an OSRAM Top LED
in order to provide a low power solution for these requirements. The tail
light also includes a photo transistor for measuring the ambient light.  
It should be tested if visibility from the side of your bike can be enhanced
by adding one LED on each side.
