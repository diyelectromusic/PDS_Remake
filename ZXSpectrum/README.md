# PDS Remake ZX Spectrum

This contains the hardware design files for the ZX Spectrum interface card for the PDS.  Based on the designs detailed here: https://www.cpcwiki.eu/index.php/PDS_development_system

# Important

Please refer to the main repository [readme](../README.md) for licensing, copyright, and limitations of use.

# Bill of Materials

* Z8420 Z80 PIO (NMOS is currently assumed given it has to work with a Z80A at 3.5MHz)
* 74LS245 octal bus transciever
* 74LS04 hex inverter
* Resistors: 1K, 4K7, 10K
* Capacitors: 3x 100nF
* 6x6x6mm tactile button switch
* SPDT slider switch 2.54mm pitch OR 2.54mm header pins and jumper
* 16-way 2x8 shrouded pin header socket
* ZX Spectrum edge connector (straight)

Assembly is all through-hole components and all components are on the same side of the board, as indicated by the silk screen printing.

KiCAD Spectrum Edge connector taken from: https://github.com/alvaroalea/8bits_kicad_libraries

Spectrum edge connectors are pretty difficult to source, but it is possible to easily get hold of a 56-way normal edge
connector and saw or grind down the two ends to make it fit a ZX Spectrum.  Then the appropriate keyed slot needs to be added
[details here](https://emalliab.wordpress.com/2026/06/12/pds-the-programmers-development-system-part-4/).

# ZX Spectrum Monitor Code

A monitor program is required to run on the ZX Spectrum to respond to commands from the PC.
Two starter versions of the monitor program are provided here, but as described in the PDS Z80 Manual,
it was typical use the provided monitor and PDS to build and download a bespoke monitor program
at a convenient location and start point in memory.

Provided sample monitors (see PDS Z80 manual for details):
* pdsdl0.tap - the PDS DL0 simple, small monitor.  Effectively only a code downloader, although filling memory works too.
* pdsdl1.tap - the PDS DL1 more full-featured monitor.

These are provided as TAP files to be used with any kind of ZX Spectrum tape emulator for loading into a real ZX Spectrum.

# License

Unless stated otherwise, all information is provided AS IS with no implied fit for purpose as detailed in the included MIT License.

Kevin
