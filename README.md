# Klayout Example Library

This code is made to demonstrate how to create a library of devices that can be used with the [SiEPIC PDK](https://github.com/lukasc-ubc/SiEPIC_EBeam_PDK/). The code includes a library registering file, a Add-Drop Ring device example, and an automatic layout creator macro.

## Requirements
- [SiEPIC PDK](https://github.com/lukasc-ubc/SiEPIC_EBeam_PDK)
- [Klayout](https://www.klayout.de/)

## Installation
- Install the SiEPIC PDK into Klayout
- Place *ExampleLibrary.lym* in your KLayout/tech/EBeam/pymacros folder
- Place *ExampleLibrary*(The Folder) in your KLayout/tech/EBeam/pymacros folder
- Place *Example_LayoutScript.lym* in your KLayout/pymacros
- Place *DEV_Library* in your KLayout/tech/EBeam/pymacros folder

## How to Use
### DEV_Library
This is an example of how to setup a library for quick proto-typing/testing of a device's code. This method **WILL** display errors if any issues arise. You can move your device's code into the organization method shown in the example library afterwards
### ExampleLibrary
This library shows how a final library can be organized to be modular. This method **WILL NOT** display errors if there are any. The advantage is to have each individual device's PCELL code and dependencies be stored as its own singular file. This way multiple same names can be used without having to worry about overlap. Furthermore it prevents accidental changes to devices that would've otherwise shared the same functions
### Example_LayoutScript
This shows how to setup a automatic layout creating script, similar to the 'dofile' used in AMPLE. Note that in this example the GC is disabled as each GC would be different size and it's dimensions are unique.

## Description
This package attempts to demonstrate a way of modularly organizing devices so that file lengths stay short making it easier to read within Klayout's native interpreter.
The package also demos how to use relative sizes to design devices that could change in size. Lastly, it shows how to draw polygons using Double-type coordinates (Dpoint).

## Known Issues
- This type of organization prevents errors from showing while scripting. It is suggested to initialize the library and design all your devices in one script first, and then finally organize them as shown in this package.
- Rounding Errors can occur due to using Double-type coordinates. Remember to check your boundaries of all polygons.
