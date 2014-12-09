PanelDue
========

This is the source code for the firmware to run the PanelDue 3D printer user interface board.

Build instructions: load file PanelDue.cppproj into Atmel Studio 6.2. For those wishing to build it under operating systems other than Windows, it should not be difficult to port it to Eclipse. The only libraries needed that are not included in this repository are the GCC toolchain libraries for the SAM3S.

Static analysis: parts of the firmware are formally verified using Escher C++ Verifier, hence the design-by-contract and other annotations. File ecv.h defines macros that make these annotations invisible to compilers.

Firmware upload instructions: see http://miscsolutions.wordpress.com/paneldue/

Submitting pull requests
========================

I will only consider pull requests that meet the following standards:
- the code must compile warning-free, with very few exceptions
- existing design-by-contract annotations must be preserved, and contracts should be added for any new functions. Please asked for a copy of eCv++ Free Edition if you plan on making substantial changes.
- the coding style must be adhered to

Acknowledgements
================

Henning Karlsen - for the original versions of the TFT display driver and the touch panel driver, see http://www.henningkarlsen.com/electronics/
Atmel - for the Atmel Software Framework, which made programming the ATSAM3S a lot easier
MikroElectronika - for prioviding GLCD Font Creator, see http://www.mikroe.com/glcd-font-creator/
Andy (kwikius) - for writing a program to compress fonts generated by GLCD Font Creator
