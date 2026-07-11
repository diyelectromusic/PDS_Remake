# PDS Remake

Design files for a remake of the PDS Programmers Development System originally developed by [Andy Glaister](https://www.glaister.com/History/Andy/Andy%20History.htm).

References:
* https://www.cpcwiki.eu/index.php/PDS_development_system
* https://trastero.speccy.org/cosas/JL/PDS/Introduccion.html
* https://lemmings.info/pds-recreating-the-system/

Blog series describing the remake: https://emalliab.wordpress.com/2026/05/04/pds-the-programmers-development-system/

The remake is happening in collaboration with [the Retro Collective](https://www.retrocollective.co.uk/) who reached out to Andy directly.  His response:

_"You absolutely have my permission to reproduce the boards, the designs and the software. I will see if I can dig up stuff to help. It would be good to see all the code again."_

We're going to try to collate as much information as we can in this repository.

# State of the Information in this Repository

| Item | Status | Notes |
| --- | --- | --- |
| ISA PC Card | Tested and Working | Details of the testing and use in [part 5](https://emalliab.wordpress.com/2026/07/10/pds-the-programmers-development-system-part-5/) and [part 6](https://emalliab.wordpress.com/2026/07/10/pds-the-programmers-development-system-part-6/) |
| ZX Spectrum Target | Tested and Working | Details also in [part 5](https://emalliab.wordpress.com/2026/07/10/pds-the-programmers-development-system-part-5/) and [part 6](https://emalliab.wordpress.com/2026/07/10/pds-the-programmers-development-system-part-6/) |
| Amstrad CPC Target | Not Tested | Has been plugged in, but that is all |

Regardless of the above, there is no expected fitness for purpose and it is strongly recommended that information or these files be used with any precious modern or retro equipment.

Only use with equipment you would be happy to use.  Proceed at your own risk.

I (Kevin) am not an electronics person.

# Key Documentation

* [The PDS Editor Manual](docs/The_PDS_Editor_Manual.pdf)
* [The PDS Z80 Manual](docs/The_PDS_Z80_Manual.pdf)

# Background (from CPC Wiki)

_PDS is an acronym for "Programmers Development System" and is a development system made by Andy Glaister. The system comprised an "Apricot PC" (an early PC), assembler, debugger, editor, profile, graphics tool and hardware to connect to a target computer. A company called "Programmers Development Systems Ltd" or "PD Systems" sold it._

_The system made it easy to develop for computers like the Amstrad CPC, C64, MSX, and ZX Spectrum. The code was written on the PC and transferred through the hardware interface to the target computer._

_The target computer ran a program which waited for PDS to send it instructions._

# Rationale

The original system is quite hard to get hold of these days, and whilst a remake was created (the trastero.speccy.org link above) at some point in the past, design information and files suitable for use with modern PCB manufacturing seem not to exist.

This is a re-documenting and remaking of some of the boards, refering to all the existing information and a reimaginging of some of the hardware components in KiCAD.

# License

The original Intellectual Property was owned by Programmers Development Systems Ltd, founded by Andy Glaister.  This new design has been put together from information obtained from the Internet, from original users of the system, and some from Andy himself, aiming to support retro enthusiasts who are not able to obtain original working hardware.

As mentioned above, we reached out to Andy about reproducing the system and he has given us the go ahead to document and publish what we're finding, consiquently everything here is publsihed under a MIT license unless stated otherwise.

**Retaining the spirit of openess and generocity shown by Andy, at this time we ask that this information is not used to create PDS hardware to be sold for commercial gain.**

Copyright of directly reproduced elements remains with the original developers.  Other elements are copyright (C) Kevin (diyelectromusic).

There is no permission, direct or implied, for the contents of this repository to be used for the training of AI systems.

Kevin
