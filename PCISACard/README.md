# PDS Remake PC ISA Card

This contains the hardware design files for the PC ISA interface card for the PDS.  Largely based on the designs detailed here: https://www.cpcwiki.eu/index.php/PDS_development_system

Although as per [my post here](https://emalliab.wordpress.com/2026/05/06/pds-the-programmers-development-system-part-2/), I don't believe the schematics published here are correct.

# Important

Please refer to the main repository [readme](../README.md) for licensing, copyright, and limitations of use.

# Bill of Materials

* Intel 8255 Parallel Peripheral Interface
* 74LS244 Octal line driver
* 74LS04 hex inverter
* 74LS138 3 to 8 decoder
* 4K7 6-pin (5+COM) resistor network
* Capacitors: 6x 100nF
* 2x 16-way 2x8 right angle shrouded pin header sockets

Assembly is all through-hole components and all components are on the same side of the board, as indicated by the silk screen printing.

# Errata

*Important Note:* Only connection 1 has been tested.  Given the design and how the second connection is wired, I don't at present understand how it was designed to work.

# PC Software

There is a PC application designed for use with a DOS based PC with an ISA slot (originally an AT or XT I believe).  There is a version for Z80 and one for 6502.  This repository only has the Z80 version - pdsz80.exe.

There are some tips for getting this running on a [486 PC running DOS 6.2 here](https://emalliab.wordpress.com/2026/07/10/pds-the-programmers-development-system-part-5/). In particular it is important to free up as much of the lower 640K memory as possible.

For full details refer to the [PDS Editor Manual](../docs/The_PDS_Editor_Manual.pdf).

# License

Unless stated otherwise, all information is provided AS IS with no implied fit for purpose as detailed in the included MIT License.

Kevin
