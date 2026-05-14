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

# License

Unless stated otherwise, all information is provided AS IS with no implied fit for purpose as detailed in the included MIT License.

Kevin
