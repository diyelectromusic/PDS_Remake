# PDS Remake Amstrad CPC

This contains the hardware design files for the Amstrad CPC interface card for the PDS.  Based on the designs detailed here: https://www.cpcwiki.eu/index.php/PDS_development_system

# Important Warning

**There is nothing official or proven or that has any expectation of fitness for purpose of any kind in this repository.**

**It is strongly recommended that none of this information is assumed to be correct and on no account should this information or these files be used with modern or retro equipment.**

Everything here is experimental at best, highly likely to be non-functioning, and at worst could damage any other equipment it is used with.  Proceed at your own risk.

Please note: I am not an electronics person.

# Bill of Materials

* Z8420 Z80 PIO (NMOS is currently assumed given it has to work with a Z80A at 3.5MHz)
* 74LS245 octal bus transciever
* 74LS04 hex inverter
* 74LS032 quad 2-input OR gate
* Resistors: 1K, 4x 4K7, 10K, 1M
* Capacitors: 4x 100nF
* 6x6x6mm tactile button switch
* SPDT slider switch 2.54mm pitch OR 2.54mm header pins and jumper
* 16-way 2x8 shrouded pin header socket
* 50-pin (2x25) edge connector (straight)

Assembly is all through-hole components and all components are on the same side of the board, as indicated by the silk screen printing.

# License

Unless stated otherwise, all information is provided AS IS with no implied fit for purpose as detailed in the included MIT License.

Also unless stated otherwise, all content and code (c) diyelectromusic (Kevin).

There is no permission, direct or implied, for the contents of this repository to be used for the training of AI systems.

Kevin
