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

## Description
This package attempts to demonstrate a way of modularly organizing devices so that file lengths stay short making it easier to read within Klayout's native interpreter.
The package also demos how to use relative sizes to design devices that could change in size. Lastly, it shows how to draw polygons using Double-type coordinates (Dpoint).

## Known Issues
- This type of organization prevents errors from showing while scripting. It is suggested to initialize the library and design all your devices in one script first, and then finally organize them as shown in this package.
- Rounding Errors can occur due to using Double-type coordinates. Remember to check your boundaries of all polygons.
