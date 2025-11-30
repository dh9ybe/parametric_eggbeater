# Parametric Eggbeater

Design and 3D-print files for eggbeater antennas

## Overview

This project is intended to enable radio amateurs and enthusiasts to easily build Eggbeater-style antennas for arbitrary frequencies.

Practically this design is usable for frequencies between about 100MHz and 1.5 GHz. At larger wavelengths, it will be very difficult to
build a mechanically stable antenna, at shorter wavelengths, the design will be too small and fiddly, so that other designs will be better
suited.

In this project, parametric, 3D-printable structural parts for the antenna design are provided. Lengths of the loop dipole and reflector
elements are calculated for the users' convenience.

The main design is made in FreeCAD Version 1.0.2. The embedded spreadsheet allows to paremetrically adapt the dimensions to the desired center
frequency and to mechanical requirements.

Printable stl files are provided in the print-bodies directories for building antennas with center frequencies of 145 MHz and 435 MHz. The
145 MHz antenna still works very well at 137 MHz for receiving weather satellite transmissions.

## Design Parameters

### Electrical

#### User Entries

|Name               | Unit | Description|
|-------------------|------|------------|
|CenterFrequency    | MHz  | the frequency for which the electrical lengths shall be computed|
|manual length      | mm   | if not zero, this length is used for the circumference of the loop diple, instead of the wavelength at CenterFrequency. Can be used with more sophisticated loop calculation methods taking into account wire diameter, conductivity etc.|
|loop length factor | N/A  | factor by which to mutliply the wavelength at CenterFrequency to compute the loop dipole circumference|

#### Computed Parameters

|Name               | Unit | Description|
|-------------------|------|------------|
|Wavelength         | mm   | Vacuum wave length at CenterFrequency|
|1/4 wave length    | mm   | quarter wave length|
|1/8 wave length    | mm   | one-eigth wave length|
|reflector distance | mm   | 1/8 wavelength rouded up to full mm|
|length of reflector rods | mm | 1.1 \* 1/4 wave length to obtail a reflector plane with 10% larger than half wave length diameter|
|loop length        | mm   | wave length scales by loop length factor|
|loop diameter      | mm   | diameter of circle with circumference of loop length|
|loop radius        | mm   | radius of circle with circumference of loop length|

### Mechanical

#### User Entries

|Name                       | Unit | Description|
|---------------------------|------|------------|
|tube outer diameter        | mm   | desired outer diameter of the main tube|
|tube thickness             | mm   | desired wall thickness of the main tube|
|minimum tube length        | mm   | do not make the tube shorter than this, even if wavelength would lead to shorter tube|
|mast mount zone length     | mm   | length of zone below reflector pattern where tube thickness is increased to allow attaching a mast clamp|
|mount zone thickness       | mm   | wall thickness in mast mount zone. the thickening is applied on the inside of the tube|
|mount lip size             | mm   | length and height of outside lip to add between mast mount zone and reflector pattern to keep main tube from slipping
from mast mounting clamp|
|cap thread length          | mm   | length of the portion of the main tube cap over the tube and length of the bottom tube plug|
|wire mount zone width      | mm   | width of the zone allowed for mounting the bottoms of the loop dipole wires and for the reflector wires|
|reflector wire diameter    | mm   | diameter of holes for mounting the reflector wires|
|loop wire diameter         | mm   | diameter if loop dipole wires, if using cylindrical loop wires|
|cap thickness              | mm   | wall thickness of the tube cap|
|cap clearance              | mm   | clearance space to allow between cap inner diameter and tube outer diameter|
|loop support holder inner diameter| mm   | diameter of the optional tube used to support the loop dipole wires|
|loop support holder height | mm   | height of the optional holder for the loop support tube to add on top of the tube cap|
|flat material loop thickness | mm   | thickness of flat material used for the loop dipole wires, if cylindrical material is not used|
|Flat meterial loop width   | mm   | thickness of flat material used for the loop dipole wires, if cylindrical material is not used|
