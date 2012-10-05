uLader
=================

This project aims at creating a backup battery powered bike
lighting system.
It borrows from the great work done by the developers of the
Forumslader and acknowledges this by incorporation
Lader (german for charger) into its name.
The u stands for the micro controller used in this design,
the use of which is going to add a lot more flexibility.

Component Overview
------------------

The uLade system consists of these components:
* main board: atmega88 uC, ac to dc circuit, charging circuit, 
control switches
* tail light: red low power led (dimmable), photo transistor
* front light: attiny uC, white low power DLR (dimmabel), white 3W led 
(dimmable), photo transistor
* 2x rotation sensor: front and back

Main Board
----------

The main board contains the circuit that converts the power input from the bike
dynamo, which acts approximately like an AC current source, to about 12V DC.
This circuit is heavily based on the awesome work done by the people behind
the Forumslader project (forumslader.de).
This circuit is also responsible for charging the LiFePo4 accumulators used.
Check out [forumnslader.de]
(http://www.forumslader.de/Akkus-fuer-12V-Lader.189.0.html) if you want to use
different batteries.
