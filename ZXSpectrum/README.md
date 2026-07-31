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
* ZX Spectrum edge connector (right angled)

Assembly is all through-hole components and all components are on the same side of the board, as indicated by the silk screen printing.

KiCAD Spectrum Edge connector taken from: https://github.com/alvaroalea/8bits_kicad_libraries

Spectrum edge connectors are pretty difficult to source, but it is possible to easily get hold of a 56-way normal edge
connector and saw or grind down the two ends to make it fit a ZX Spectrum.  Then the appropriate keyed slot needs to be added ([details here](https://emalliab.wordpress.com/2026/06/12/pds-the-programmers-development-system-part-4/)).

# Errata

* The enable switch is the opposite sense to the original.  To be honest it is probably best replaced with a 3-pin jumper header anyway.
* Using a straight edge connector does not leave enough space between the connector and components to fit a Spectrum.

# ZX Spectrum Monitor Code

A monitor program is required to run on the ZX Spectrum to respond to commands from the PC.
Two starter versions of the monitor program are provided here, but as described in the PDS Z80 Manual,
it was typical to use the provided monitor and PDS to build and download a bespoke monitor program
at a convenient location and start point in memory.

Provided sample monitors (see the [PDS Z80 manual](../docs/The_PDS_Z80_Manual.pdf) for details):
* pdsdl0.tap - the PDS DL0 simple, small monitor.  Effectively only a code downloader, although filling memory works too.
* pdsdl1.tap - the PDS DL1 more full-featured monitor.

These are provided as TAP files to be used with any kind of ZX Spectrum tape emulator for loading into a real ZX Spectrum.

Details of how these TAP files were produced can be [found here](https://emalliab.wordpress.com/2026/07/10/pds-the-programmers-development-system-part-6/) and the slightly modified versions of the code that were used are in the .z80 files in this repository.

There are also two WAV audio files that have been produced using https://www.igormaznitsa.com/tap2wav/index.html.

It can be quite problematic playing WAV or MP3 files into a Spectrum however.  Modern digital devices just don't have the output levels required.  There is a great discussion, and neat solution, described here: https://retrocomputing.stackexchange.com/questions/773/loading-zx-spectrum-tape-audio-in-a-post-cassette-world

But if you can play these files through some kind of amplification, they might work.

It is also possible to use the following BASIC as a type-in DL0 loader running at address 32768:

```
5 CLEAR 32760
10 LET a=32768
20 READ n: POKE a,n
30 LET a=a+1: GOTO 20
40 DATA 243, 62, 255, 211, 127, 211, 63, 62
45 DATA 63, 211, 127, 62, 255, 211, 95, 211
50 DATA 95, 22, 64, 205, 90, 128, 123, 254
55 DATA 180, 202, 51, 128, 254, 183, 202, 80
60 DATA 128, 254, 181, 194, 19, 128, 205, 90
65 DATA 128, 99, 205, 90, 128, 107, 1, 19
70 DATA 128, 197, 233, 205, 90, 128, 99, 205
75 DATA 90, 128, 107, 205, 90, 128, 67, 205
80 DATA 90, 128, 75, 205, 90, 128, 115, 35
85 DATA 11, 120, 177, 194, 67, 128, 24, 195
90 DATA 205, 90, 128, 1, 253, 127, 237, 89
95 DATA 24, 185, 219, 63, 170, 15, 218, 90
100 DATA 128, 219, 31, 95, 122, 211, 63, 238, 129, 87, 201
```

Once loaded, run the basic program until you see an "Out of Data" error.  This loads the machine code which can then itself be run.

```
RUN
PRINT USR 32768
```

# License

Unless stated otherwise, all information is provided AS IS with no implied fit for purpose as detailed in the included MIT License.

Kevin
