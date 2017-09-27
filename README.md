# ArduinoFlashProgrammerV2
Arduino based Flash Memory Programmer - Version 2

The first version of my Flash memory programmer revealed a couple of basic flaws, the main one being the size of the sectors
in the chips I was using (64k) and the fact that I would be needing to program only half of this at a time.

Simple solution - 64k of static RAM to hold a complete sector, allowing the sector to be read out, the new code to be merged
and then the sector erased and written back.

Problem - The original design had not left enough spare pins and had also used the SPI pins on the Mega as general I/O so
Version 2 was conceived. In this version, the SPI pins are made available for the serial SRAM to use and the high bit selection
lines and LEDs are moved onto PortK. A new PCB is planned with a bit more room for a ZIF socket (the old one used to hang over
the sides of the board) and the SRAM chip. Software will need some new commands as well.

Now to see if I can get this all designed and working.....
