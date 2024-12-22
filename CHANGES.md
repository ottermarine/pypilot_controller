These design files constitute a modified version of a work licenced
under the Creative Commons "Attribution-ShareAlike 4.0 International"
(CC-BY-SA-4.0) license.

This file documents changes made since distribution by the original
author, Sean D'Epagnier.

# 2024-12-16  Mitch Davis  <mjd@afork.com>

 - We no longer need this file (`freetronics_schematic.kicad_sym`).
 - Switching to markdown format for the licence
 - Added text to silkscreen on front and back with authorship, licence and websites
 - Refilled zones
 - Made a small tweak to add another thermal relief to ground zone
 - Updated fuse footprint to have LCSC numbers
 - Added symbols for mounting and cable tie holes, to avoid warning on import from schematic
 - Added a board stack-up, plus some gerber settings
 - Changes KiCad keeps wanting to make to the project file 
   (plus some settings from the original dump)
 - Update all symbols.  That it produced so little change confirms very little
   divergence from stock and custom symbols.  Yippee!
 - Update footprints on PCB for 0805 caps
 - Update footprints on PCB for 1206 capacitors
 - Update footprints on PCB for electrolytics
 - Fix a courtyard clearance problem
 - Update footprints on PCB for headers
 - Pull from schematic, and update charge pump diodes, regulators and SOT-23-5 translators
 - Rework the opto circuit with smaller caps to reduce clutter.
 - Add a hidden pin 1 to 74LVC1G17 symbol, and move power pins so
   wires can be connected in schematic editor
 - Update every symbol in the schematic
 - Oops, should hide datasheet and footprint fields in TVS symbol
 - Switch from using AMS1117-5.0 to XC6202P502FR-G 5V 200mA LDO regulator.
   (This is what's in the CSV file as the regulator that's being used)
 - Fixed pin number problem on XC6202P502FR-G 5V regulator symbol
 - Switch the charge pump diode symbol to the part that's actually being used
 - Add ES2G diode and XC6202P502FR-G 5V 200mA LDO regulator to symbols
 - Updated footprint on PCB for ISP header
 - Updated symbol for ISP header.
   (Numbering was still set to old order)
 - Update footprints on PCB for gate driver charge pump SMA package diodes.
   (Expanded courtyard reqiured moving components a little)
 - Update footprints on PCB for 0603 LED
 - Update footprints on PCB for 0805 LEDs
 - Update footprint on PCB for TQFP-32 ATmega328P
 - Update footprints on PCB for SO-5 package optos.
 - Update footprints on PCB for SOIC-8 gate drivers
 - Updated footprint on PCB for AMS1117
 - Update footprints on PCB for everything with a TO-252-2 footprint
 - Update footprint on PCB for TVS diodes
 - Modified silkscreen of TVS footprint to not be so wide
 - Updated footprint on PCB for F1 fuse
 - Fix drill size I messed up
 - Update footprints on PCB for screw terminals, and
   fixed inconsistent alignment and track widths
 - Remove silkscreen from footprint holes
 - Remove silkscreen from screw terminal holes
 - Update footprints for 0805 resistors on PCB
 - Update footprint on PCB for R1, PSU ballast resistor
 - Update footprint on PCB for R20, the shunt resistor

2024-12-15  Mitch Davis  <mjd@afork.com>

 - Updated UART footprint
   (Esp the silk, and taking things off Eco1 layer)
 - Fixed MOSFET positions
   (New footprint has a different centroid)

2024-12-14  Mitch Davis  <mjd@afork.com>

 - Shifted MOSFET locations to match original board
   (Centroid varies from original footprint)
 - Rename old nets from KiCad 5 PCB to match net names
   coming from schematic in KiCad 8.
   (KiCad has changed its algorithm for naming nets)

2024-12-12  Mitch Davis  <mjd@afork.com>

 - First pull of new footprints and net info from schematic to PCB
   (It's obviously broken, many footprints aren't oriented or placed
   correctly)
 - Fix missing wires around smaller cap symbols
 - Add sheets to project file
 - Add missing designators to schematic

2024-12-09  Mitch Davis  <mjd@afork.com>

 - Fix symbol for ISP header
 - Replace 74AHC1G125 with 74LVC1G17

2024-12-08  Mitch Davis  <mjd@afork.com>

 - Removed fab layers.  (In this day and age of PnP machines,
   it's just noise)
 - First save of PCB with KiCad 8
   Gerbers are equivalent to originals

2024-12-07  Mitch Davis  <mjd@afork.com>

 - Patch in particular TVS model numbers
 - Reconnect caps
   (Stock symbols are smaller than the Freetronics ones were)
 - Move the UART header symbol from the uart sym lib to pypilot_components sym lib
 - Use stock KiCad symbols instead of Freetronics ones.
 - Adjusted power pins on 74AHC1G125
 - Move footprints into pypilot\_controller\_footprints, creating from PCB file if missing.
 - Switch footprints to stock KiCad versions, if the stock one is equivalent
 - Fix tlp2631 symbol recommended footprint from Package\_SO:SO-6 to Package_SO:SO-5

2024-12-06  Mitch Davis  <mjd@afork.com>

 - Replaced .sch schematics with new-style .kicad_sch equivalents
 - UART connector sym lib converted to new format
 - Remove old sym lib with rescued symbols
   All symbols in use have been carefully crosschecked to KiCad's stock
   symbols for differences.
 - Switch to new style local symbol libs
 - Switch to stock KiCad symbols that exist
 - Switch VCC to pypilot_controller symlib
   Because KiCad's VCC is an arrow, whereas the one that came with PyPilot
   is a circle.  The VCC in pypilot_controller is the circle one.
 - Provide missing freetronics_schematic and pypilot_components symbol libraries
   Recovered from pypilot_controller-rescue.kicad_sym, then converted to
   .kicad_sym format.

2024-12-05  Mitch Davis  <mjd@afork.com>

 - Attempt to merge settings from .pro and .kicad_pro
 - Ignore /old/ subdir
 - Files as received from Sean
 - Initial commit, as received from Sean
