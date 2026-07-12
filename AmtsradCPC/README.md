# PDS Remake Amstrad CPC

This contains the hardware design files for the Amstrad CPC interface card for the PDS.  Based on the designs detailed here: https://www.cpcwiki.eu/index.php/PDS_development_system

# Important

Please refer to the main repository [readme](../README.md) for licensing, copyright, and limitations of use.

***This design is, as yet, completely untested.***

# Bill of Materials

* Z8420 Z80 PIO (NMOS is currently assumed given it has to work with a Z80A at 4MHz)
* 74LS245 octal bus transciever
* 74LS04 hex inverter
* 74LS032 quad 2-input OR gate
* Resistors: 1K, 4x 4K7, 10K, 1M
* Capacitors: 4x 100nF
* 6x6x6mm tactile button switch
* SPDT slider switch 2.54mm pitch OR 2.54mm header pins and jumper
* 16-way 2x8 shrouded pin header socket
* 50-pin (2x25) edge connector (right angle)

Assembly is all through-hole components and all components are on the same side of the board, as indicated by the silk screen printing.

# Errata

Apart from the fact this is completely untested and might not work at all...

* The enable switch is the opposite sense to the original.
* Using a straight edge connector does not leave enough space between the connector and components to fit a CPC.

# License

Unless stated otherwise, all information is provided AS IS with no implied fit for purpose as detailed in the included MIT License.

Kevin
