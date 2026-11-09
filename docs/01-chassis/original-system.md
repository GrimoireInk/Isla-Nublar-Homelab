# Original Gateway System

## Status

**In Progress**

## Purpose

This document records the Gateway computer in its original condition before teardown.

The goal is to preserve enough information to:

- Identify the original system
- Understand how the chassis was designed
- Record the original component layout
- Preserve front-panel wiring information
- Compare the legacy platform with the final NUBLAR-CORE build
- Provide before/after portfolio documentation

## System Identification

A rear factory label identifies the system/chassis as:

- **Manufacturer:** Gateway
- **Label designation:** `LP MINI TOWER TB3 Essential 500`
- **Product family:** Gateway Essential 500
- **Label date:** `11/20/99`
- **Form-factor wording on label:** LP Mini Tower
- **Regulatory markings:** FCC, CE, VCCI and other certification marks are visible

A unique serial/asset-style number is present on the factory label and on a smaller side-panel label. Those identifiers are intentionally not reproduced in this public repository because they currently provide no technical value.

## Initial Visual Condition

The system is a legacy beige Gateway desktop tower with:

- Gateway branding on the lower front panel
- An optical drive
- A 3.5-inch floppy drive
- Multiple unused front drive-bay covers
- A removable side panel
- A factory rectangular perforated ventilation field in the removable side panel
- A legacy motherboard
- A legacy CPU cooling assembly
- A legacy power supply
- Internal ribbon cabling
- Multiple expansion slots and expansion cards
- Internal drive mounting hardware

The case shows cosmetic wear consistent with its age but appears structurally suitable for restoration and modification.

### Removable Side Panel

The removable metal side panel has been photographed separately.

Observed features:

- Original beige/ivory textured finish
- Factory rectangular perforated ventilation field
- Minor surface scratches and age-related cosmetic wear
- A partially worn **QUALITY** inspection sticker near the lower edge
- A small numeric identification label near another lower corner

No major bending, punctures, or structural damage are visible in the supplied photographs.

## Initial Safety Decision

The original PSU will not be reused for the final NUBLAR-CORE build.

Reasons include:

- Age
- Unknown electrical condition
- Lack of modern power connectors
- Reliability requirements for HomeLab operation
- Potential incompatibility with modern hardware

The PSU housing must not be opened during teardown.

## Original Component Inventory

Complete this inventory before components are discarded, recycled, or repurposed.

| Component | Manufacturer / Model | Visible Part Number | Notes |
|---|---|---|---|
| Chassis / System | Gateway Essential 500 | LP MINI TOWER TB3 Essential 500 | Rear label dated 11/20/99 |
| Motherboard | TBD | TBD | Installed |
| CPU | TBD | TBD | Installed under legacy cooler |
| CPU cooler | TBD | TBD | Installed |
| Memory | TBD | TBD | To be inventoried |
| Power supply | TBD | TBD | Do not open; not planned for reuse |
| Optical drive | TBD | TBD | Installed |
| Floppy drive | TBD | TBD | Installed |
| Storage drive(s) | Western Digital Caviar 102AA, model WD102AA-53AAA4 | 10262.5 MB / 10.2 GB | Removed and identified; 3.5-inch Enhanced IDE hard drive dated 10 Nov 1999 |
| Expansion card 1 | 3Com / U.S. Robotics Model 0637 56K PCI Voice WinModem | 1.012.0637-D / 6001126 / PCB label 1.028.0470-10 | Removed and identified; dual RJ-11 LINE IN / TO PHONE ports |
| Expansion card 2 | Creative Labs CT5803 Sound Blaster AudioPCI 64 (Dell/Gateway OEM) | 6001238 / A5170652 / ASSYNO: 4 REV:A | Removed and identified; PCI sound card with 3x 3.5 mm audio jacks and DB-15 game/MIDI port |
| Expansion card 3 | VisionTek NV996.0 Rev. D NVIDIA RIVA TNT2 M64 / Vanta AGP graphics card | Gateway 6001425 / G7500.1 | Removed and identified; 8 MB AGP card with single VGA output |\n| Additional cards | TBD | TBD | To be inventoried |


## Expansion Card 1 — 3Com / U.S. Robotics 56K PCI WinModem

The first removed expansion card has been identified as a 3Com / U.S. Robotics Model 0637 internal PCI modem.

### Visible Identification

- **Manufacturer:** 3Com / U.S. Robotics
- **Model:** 0637
- **Function:** 56K internal PCI Voice WinModem
- **Board marking:** `1.012.0637-D`
- **Gateway/OEM-compatible part marking:** `6001126`
- **Additional PCB label:** `1.028.0470-10`
- **Copyright marking:** 3Com, 1998
- **External connectors:** Two RJ-11 telephone jacks
  - `LINE IN`
  - `TO PHONE`
- **Bus:** PCI
- **Regulatory markings:** FCC, Industry Canada, VCCI and other certification markings visible

The card was photographed in its original installed position and again after removal, including both sides of the PCB and the rear bracket.

The modem will not be reused in the modern NUBLAR-CORE system, but it is being retained temporarily as part of the original-system record.



## Expansion Card 2 — Creative Labs CT5803 Sound Blaster AudioPCI 64

The second removed expansion card has been identified as a Creative Labs CT5803 PCI sound card. Creative's official product list identifies CT5803 as the **Sound Blaster Audio PCI 64 Dell/Gateway OEM** model.

### Visible Identification

- **Manufacturer:** Creative Technology / Creative Labs
- **Model:** `CT5803`
- **Product family:** Sound Blaster AudioPCI 64
- **OEM association:** Dell / Gateway
- **Interface:** PCI
- **Assembly marking:** `ASSYNO: 4 REV:A`
- **OEM/part marking:** `6001238`
- **Additional label:** `A5170652`
- **Additional board marking:** `AudioPCI9942`
- **Assembly location:** Singapore
- **External connectors:**
  - Green 3.5 mm audio jack
  - Black 3.5 mm audio jack
  - Pink 3.5 mm microphone jack
  - DB-15 game/MIDI port
- **Internal headers:** Multiple internal audio/CD auxiliary headers are visible along the top edge

The card was photographed after removal, including the component side, solder side, and rear bracket.

The card will not be reused in the modern NUBLAR-CORE system but is being retained temporarily as part of the original-system record.



## Expansion Card 3 — VisionTek NV996.0 Rev. D NVIDIA RIVA TNT2 M64 / Vanta

The third removed expansion card has been identified as a VisionTek NV996.0 Rev. D AGP graphics card built around NVIDIA's RIVA TNT2 M64 GPU.

### Visible Identification

- **Manufacturer:** VisionTek
- **Board model:** `NV996.0`
- **Board revision:** `REV. D`
- **GPU:** NVIDIA RIVA TNT2 M64
- **Gateway part number:** `6001425`
- **Gateway/OEM board family marking:** `G7500.1`
- **Video memory:** 8 MB
- **Interface:** AGP
- **External output:** Single 15-pin VGA connector
- **VGA BIOS label:** `V2.05.13.04`

The GPU itself is marked **RIVA TNT2 M64**, while Gateway's legacy support documentation identifies part number `6001425` as an **8 MB Vanta TNT-2** adapter. The documentation therefore retains both names so the physical silicon marking and OEM product designation are both represented accurately.

The card was photographed after removal from both sides and at the rear bracket.

The graphics card will not be reused in the modern NUBLAR-CORE system but is being retained temporarily as part of the original-system record.



## Storage Drive — Western Digital Caviar 102AA

The original hard drive has been removed and identified.

### Visible Identification

- **Manufacturer:** Western Digital
- **Series:** Caviar 102AA
- **Model:** `WD102AA-53AAA4`
- **Capacity:** `10262.5 MB` (approximately 10.2 GB)
- **Interface:** Enhanced IDE / PATA
- **Form factor:** 3.5-inch
- **Manufacturing date on label:** `10 NOV 1999`
- **Power:** Standard legacy 4-pin peripheral power connector
- **Data connector:** 40-pin IDE
- **Jumper block:** Master / Slave / Single settings are printed on the factory label
- **Country of manufacture:** Malaysia

The drive's unique serial number is intentionally omitted from the public documentation because it provides no technical value to the project.

External historical references for the Caviar 102AA family describe it as a 5400 RPM ATA/IDE drive in the 10.2 GB class.

The drive will not be used as primary storage in the modern NUBLAR-CORE build. It is being retained temporarily as part of the original-system record.


## Labels to Record

Before teardown, photograph and transcribe any readable:

- [x] Gateway model/system label
- [x] Gateway serial / service label photographed; unique identifier not published
- [ ] Motherboard model
- [ ] PSU model
- [ ] Optical drive model
- [ ] Floppy drive model
- [x] Storage drive label — Western Digital Caviar 102AA documented
- [x] Expansion-card labels — Cards 1, 2, and 3 identified; remaining cards pending
- [x] Regulatory labels / certification marks
- [ ] Internal assembly labels
- [ ] Front-panel wiring labels

Sensitive identifiers that add no educational value may be omitted or redacted before publication.

## Required Pre-Teardown Photographs

- [x] Exterior front
- [x] Interior side view
- [x] Exterior rear
- [x] Removable side panel exterior
- [x] Rear factory system label
- [ ] Opposite exterior side
- [ ] Top
- [ ] Bottom
- [x] Motherboard photographed in place before removal; detailed model identification still pending
- [x] CPU cooler visible in pre-removal documentation; exact model still pending
- [ ] PSU label
- [ ] Optical drive label
- [ ] Floppy drive label
- [ ] Storage drive labels
- [x] Expansion card 1 — photographed installed and after removal
- [x] Expansion card 2 — photographed after removal
- [x] Expansion card 3 — photographed after removal
- [ ] Remaining expansion cards
- [ ] Front-panel connectors at motherboard
- [ ] Power connectors before disconnection
- [ ] Data-cable routing
- [x] Drive-cage mounting points photographed during removal

## Teardown Rule

Because several internal labels and connectors are obstructed by the compact chassis layout, identification will be performed progressively during teardown.

Before removing each component:

1. Photograph its installed position and any visible connections.
2. Disconnect and remove only that component.
3. Photograph all newly exposed labels, connectors, mounting points, and surrounding hardware.
4. Record the component identification before continuing to the next item.

This staged approach preserves the original layout while allowing hidden model numbers and wiring to be documented safely.

## Next Step

Begin controlled staged teardown. Start with the most accessible removable component, document it before and after removal, then update the inventory before continuing.
