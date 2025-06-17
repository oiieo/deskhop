# DeskHop v1.1 PCBWay Assembly Instructions

## Overview
This folder contains the necessary files for PCBWay to manufacture and assemble the DeskHop v1.1 PCB.

## Files Included

1. **Gerber Files** (in Gerber/ folder):
   - Already included in the project
   - Use the existing `Gerber_DeskHop.zip` file

2. **Bill of Materials (BOM)**:
   - `DeskHop_v1.1_BOM_PCBWay.csv` - Standard format for PCBWay
   - `DeskHop_v1.1_BOM_Extended.csv` - Extended format with additional details

3. **Pick and Place File**:
   - `DeskHop_v1.1_PickAndPlace.csv` - Template file (actual coordinates need to be exported from KiCad)

## PCB Specifications

- **Layers**: 2
- **PCB Thickness**: 1.6mm (IMPORTANT: Required for case fit)
- **Surface Finish**: HASL or ENIG
- **Solder Mask**: Green (or your preference)
- **Silkscreen**: White

## Assembly Notes

### SMD Components (for PCBWay assembly):
All SMD components are on the TOP side only:
- U3, U5: TPD4E1U06DBVR (SOT-23-6)
- U4: ISO7721DR (SOIC-8) 
- C1, C2: 100nF 0805
- C3, C4: 4.7uF 0805
- R1-R4: 27Ω 0805

### Through-Hole Components (typically hand-soldered):
- U1, U2: Raspberry Pi Pico boards
- J1, J4: USB-A female connectors
- J2, J3: 1x3 pin headers

## Important Notes for PCBWay

1. **Component Orientation**: Pay special attention to the orientation of:
   - U3, U5 (SOT-23-6 packages) - Pin 1 marking
   - U4 (SOIC-8) - Pin 1 marking

2. **Alternative Components**:
   - U4 can be substituted with ADuM1201BRZ if ISO7721DR is not available (pin-compatible)

3. **Special Requirements**:
   - Apply conformal coating or flux cleaning after assembly to prevent corrosion
   - Visual inspection of all solder joints, especially on the fine-pitch components

## Ordering Process

1. Upload the Gerber files from `Gerber_DeskHop.zip`
2. Select "PCB + Assembly" service
3. Upload the BOM file: `DeskHop_v1.1_BOM_PCBWay.csv`
4. For pick and place data:
   - Either export from KiCad: File -> Fabrication Outputs -> Component Placement (.pos)
   - Or let PCBWay generate it from the Gerber files

5. Specify:
   - SMD assembly on TOP side only
   - Lead-free process preferred
   - 100% electrical testing if available

## Contact Information

For any questions about the assembly, refer to:
- Original project: https://github.com/hrvach/deskhop
- Schematic: /schematics/DeskHop_v1.1.pdf

## Version History

- v1.1: Current version with ESD protection and improved layout
- v1.0: Original version (simpler but without ESD protection)