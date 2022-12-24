⚠ Incomplete / Alpha as of December 2022.

# Ender to Switchwire Conversion + IDEX

Conversion of Ender 3 Pro/V2 to a Customized Voron Switchwire. Since most of the Creality stuff gets deleted, It's probably the same amount of work and cost to use the CR-10, CR-10S as donor machines as well.

## Adapted from laudable the work of:
* [Triano's original Ender to Switchwire conversion](https://github.com/walttriano/VoronUsers/tree/master/printer_mods/Triano/Ender_3Pro_Switchwire)
* [boubounokefalos update of Triano's design](https://github.com/boubounokefalos/Ender_SW)
* [ankur2k6 IDEX mod](https://github.com/ankurv2k6/voron_idex_switchwire)
* [VOV0 by Mamish](https://github.com/Mamsih/VOV0-toolhead-voron-Zero) which is adapted from [HextrudORT by MirageC](https://miragec79.github.io/HextrudORT/)

## Redesign Goals + Use-Case Considerations
* Increase print bed size for specific project
* Install in separate insulated chamber (delete Voron enclosure)
* Move control electronics and power supply outside enclosure
* Improve speed and quality of bedslinger
* Economy of filament for upgrade parts > Voron branding (delete Voron grills)
* Toolhead weight reducion > Voron aesthetics (No Stealth/Afterburner. Adapt 

## Design by boubounokefalos ***prior to modifications and IDEX***
![Home](Images/non_enclosed.png)

## Major Changes
* Increase print bed to 400mm x 600mm (using two 400 x 300 silicone heater pads)
* Increase Y stability by replacing 3030 (Switchwire) and 4040 (Ender) Y-axis with OpenBuilds 4080 C-Beam
* Upgrade Y motion speed and accuracy with Nema23 or dual Nema17 and closed loop board(s)
* Delete milled 4040 Center Beam of Ender base and replace with Front and Rear Crossbeam (2020 or 2040)

## Toolhead Changes
* Replace Mosquito with DropEffect/Phaetus XG
* Add Phaetus APUS extruder compatibility
* Add aluminum Vz-Hextrudort (by Vez3d / MirageC) compatibility

## IDEX Notes
***Status: WIP to assess adapted kinematics between Dual Markforged, haqXY, coreXYU, etc.***
ankurv2k6 has a very cool functional IDEX build, and has done a great job of providing the necessary STL files in the IDEX mod repository. At the time of this writing, there are no images or instructions for assembling the modified XZ, gantry, IDEX, et cetera.

## Info

## BOM
Currently in a messy Google doc as I make sure the Voron Switchwire BOM and others haven't changed since the repos I've forked have mostly been inactive since 2021. Will publish here when readable to normal humans.

Various parts _can*_ be recycled from the Ender 3 Pro/V2, CR-10 series. The most important are:
- The frame (though a 310mm extrusion is needed for the X. You can chop the original one to length).
- The MeanWell PSU - 24V from Ender3 Pro/V3, not 12V from CR-10 & CR-10S
- ~~The heatbed assembly.~~ Only if using stock build size
- The original board. Maybe.
- XYZ motors (as long as you can pull off the pulleys. Additional Nema14 (20mm) motor is needed for printhead extruder options).
- All the cables that don't go through the cable-chains (for there, silicone or PTFE cable is adviced).
- 4010 fan for the tool cooling.

*cheaping out in parts can lead into several problems, such as poor printing quality or, even worse, safety hazard. Keep that in mind and use parts from the official Switchwire BOM.

## Files

- Most of the printed part files needed for this conversion, are included in this git (you will only need to get the Afterburner print files from the [official Switchwire git](https://github.com/VoronDesign/Voron-Switchwire/tree/master/STL/Gantry/XZ_Axis/X_Carriage) ).
- CAD files (.f3d and .STEP) are provided, in order to help the building process, but they also serve as a BOM (in case you need to find proper screw lengths etc).
- DXF files in order to cut your enclosure panels.
- A printer.cfg as a starting point (based off LDO motors and SKR E3 mini V2 board).

## Status


## Credits

- Ofc to Triano for his awesome design and all the valuable help, info and support.
- To marcel#0874 for his original idea of the sticky grill endcaps.
- To sdukan#9213 for his valuable help into troubleshooting the Ender 3 V2 differences, electronics (and in general)
- To all of this awesome community of people.
- To Voron design team for all the valuable resources and the solid base.

## Disclaimer

This is a carefuly designed build, but currently in ALPHA
