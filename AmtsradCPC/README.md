# PDS Remake Amstrad CPC

This contains the hardware design files for the Amstrad CPC interface card for the PDS.  Based on the designs detailed here: https://www.cpcwiki.eu/index.php/PDS_development_system

# Important

Please refer to the main repository [readme](../README.md) for licensing, copyright, and limitations of use.

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

* The enable switch is the opposite sense to the original.
* Using a straight edge connector does not leave enough space between the connector and components to fit a CPC.

# Amstrad CPC Monitor Code

A monitor program is required to run on the CPC to respond to commands from the PC.
A starter version of the monitor program is provided here
(see [part 8](https://emalliab.wordpress.com/2026/08/16/pds-the-programmers-development-system-part-8/)
for details, but as described in the PDS Z80 Manual,
it was typical to use the provided monitor and PDS to build and download a bespoke monitor program
at a convenient location and start point in memory.

The following BASIC is a type-in DL0 loader running at address &8000:

```
  5 SYMBOL AFTER 256: MEMORY &7FFF: SYMBOL AFTER 240
 10 LET a=&8000
 20 READ n: POKE a,n
 30 LET a=a+1
 40 GOTO 20
100 DATA &3E,&FF,&01,&EE, &FB,&ED,&79,&ED
105 DATA &79,&0C,&ED,&79, &0E,&ED,&ED,&79
110 DATA &0E,&EF,&3E,&3F, &ED,&79,&16,&40
115 DATA &F3,&CD,&60,&80, &7B,&FE,&B4,&CA
120 DATA &43,&80,&FE,&B7, &CA,&39,&80,&FE
125 DATA &B5,&C2,&19,&80, &CD,&60,&80,&63
130 DATA &CD,&60,&80,&6B, &01,&19,&80,&C5
135 DATA &E9,&CD,&60,&80, &06,&7F,&4B,&ED
140 DATA &49,&18,&D6,&CD, &60,&80,&63,&CD
145 DATA &60,&80,&6B,&CD, &60,&80,&43,&CD
150 DATA &60,&80,&4B,&CD, &60,&80,&73,&23
155 DATA &0B,&78,&B1,&C2, &53,&80,&18,&B9
160 DATA &C5,&01,&ED,&FB, &ED,&78,&AA,&0F
165 DATA &DA,&64,&80,&0D, &ED,&58,&0C,&7A
170 DATA &ED,&79,&EE,&81, &57,&C1,&C9
```

Once loaded, run the basic program until you see an "Out of Data" error.
This loads the machine code which can then itself be run.

```
RUN
CALL &8000
```

# License

Unless stated otherwise, all information is provided AS IS with no implied fit for purpose as detailed in the included MIT License.

Kevin
