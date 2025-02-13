# Overview
This project provides a Pi Zero hat which allows a Raspberry Pi to be connected to a BBC Micro or Master via the 1 MHz bus port.  The hat is compatible with all versions of the Raspberry Pi (with 40 pin GPIO headers)

Since the BBC Micro is 5Vs and the Pi is 3.3Vs bi-directional level shifting is required.  In addition, the board provides an active audio buffer to allow the Pi Zero to output audio via the GPIO header.  Audio is routed into the BBC Micro if the audio jack isn't required.

# Production
Production files for JLCPCB.com are included for both the PCB and component assembly.  A custom DRC is also included that checks the project files against JLC's production rules.  Production files can be found in the repo:

https://github.com/simoninns/acorn_1mhz_bus_pi_if/tree/main/kicad/jlcpcb

# Use with Raspberry Pi 3B+
Some Raspberry Pi models will not boot due to leakage on the 3.3V rails - the project provides a jumper that can be set if you want to use on of the affected models.  JP3 pins 1 to 2 should be cut and a solder blob placed on 2-3.  Please see the schematic for details.

# Removal of active audio
To lower production cost the on-board LDO and buffer ICs can be omitted (as well as the audio jack).  Bridging JP1 and JP2 will bypass the active components and provide only a passive audio filter (this works fine but provides a poorer sound quality).

## Project status
This project is at first release.  Please read the wiki and see YouTube for consruction videos (detailed in the wiki also).

## Author
This project is designed and maintained by Simon Inns with help from Dominic Plunkett and Daniel Jameson.

## Software License (GPLv3)

    This is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    Valiant Turtle 2 is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see <http://www.gnu.org/licenses/>.

## Hardware License (Creative Commons BY-SA 4.0)
Please see the following link for details: https://creativecommons.org/licenses/by-sa/4.0/

You are free to:

Share - copy and redistribute the material in any medium or format
Adapt - remix, transform, and build upon the material
for any purpose, even commercially.

This license is acceptable for Free Cultural Works.

The licensor cannot revoke these freedoms as long as you follow the license terms.

Under the following terms:

Attribution - You must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.

ShareAlike - If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original.

No additional restrictions - You may not apply legal terms or technological measures that legally restrict others from doing anything the license permits.
