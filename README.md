# Snapmaker2Postprocessor

## Overview
This project provides a postprocessor for the [Path Workbench](https://wiki.freecadweb.org/Path_Workbench) of [FreeCAD](https://www.freecad.org) compatible with the CNC module of [Snapmaker 2.0](https://snapmaker.com) machines.

It converts FreeCAD internal GCODE generated by the Path Workbench into GCODE suitable for Snapmaker 2.0 machines.
Its functions cover:
- Snapmaker CNC commands
- tool change between operations (by inserting a HMI pause (M76))
- drilling (by converting G81-G83 commands)
- thumbnail generation for HMI
- rapid moves (speed is not added by FreeCAD to GCODE)

## Usage
Move the `Snapmaker_2.0_CNC_post.py` file to the FreeCAD macros directory. It should appear within the list of postprocessors of the Path workbench. 

Check the [wiki](https://github.com/clsergent/Snapmaker2Postprocessor/wiki) if you need more information.

Refer to [FreeCAD documentation](https://wiki.freecadweb.org/Path_Post) on how to use a postprocessor.


## Limitations
This postprocessor has been tested on FreeCAD 0.20 shipped with python3.10.
Generated GCODE has only been tested on a Snapmaker 2 A350. It *should* work on any other Snapmaker 2.0 (A150, A250, A250T, A350T), and *may* work on other Snapamker machines, but with no warranty.
If you encounter any bug, please open an issue. 


## Credits
Parts of this postprocessor have been inspired by the Marlin postprocessor shipped along with [FreeCAD](https://www.freecad.org).

## License
This repository and its content are licensed under the EUPL-1.2-or-later.

Check https://joinup.ec.europa.eu/collection/eupl/eupl-text-eupl-12

This license is deemed to be compatible with the one used by FreeCAD.
