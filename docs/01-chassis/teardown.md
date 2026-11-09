# Gateway Teardown Log

## Status

**Not Started**

## Objective

Safely remove the original Gateway components while preserving a complete visual and written record of how the system was assembled. Because some labels and connectors are physically blocked, component identification will occur progressively as each layer of hardware is removed.

## Safety

- Disconnect AC power before beginning.
- Do not work inside the system while connected to mains power.
- Do not open the PSU enclosure.
- Use appropriate electrostatic-discharge precautions when handling components.
- Do not force brittle legacy plastic clips or connectors.
- Keep removed screws and hardware organized by component.

## Teardown Sequence

### Step 1 — Pre-Teardown Documentation

- [x] Photograph untouched interior from multiple angles
- [x] Record rear factory system label and model designation
- [ ] Photograph any currently visible connectors, cables, and component positions
- [ ] Record currently visible internal labels

Hidden labels and wiring will be documented progressively as components are removed.

### Step 2 — Expansion Cards

**Progress:** In Progress — Cards 1, 2, and 3 removed and identified.

For each card:

- Photograph before removal
- Record slot position
- Remove the card
- Photograph both sides after removal
- Record manufacturer/model and part numbers once visible
- Label/store the card before continuing

| Card | Original Slot | Identification | Notes |
|---|---|---|---|
| Expansion Card 1 | PCI slot (exact slot number to be confirmed after full motherboard exposure) | 3Com / U.S. Robotics Model 0637 56K PCI Voice WinModem, 1.012.0637-D | Removed successfully; photographed both sides and bracket |
| Expansion Card 2 | PCI slot (exact slot number to be confirmed after full motherboard exposure) | Creative Labs CT5803 Sound Blaster AudioPCI 64, 6001238, ASSYNO: 4 REV:A | Removed successfully; photographed component side, solder side, and bracket |
| Expansion Card 3 | AGP slot | VisionTek NV996.0 Rev. D, NVIDIA RIVA TNT2 M64 / Vanta, Gateway 6001425, G7500.1 | Removed successfully; photographed both sides and VGA bracket |

### Step 3 — Drives

**Progress:** In Progress — original hard drive removed and identified.

For each drive:

- Photograph cables and mounting method
- Record manufacturer/model
- Disconnect data and power
- Remove mounting screws or rails
- Store safely

| Drive | Bay | Identification | Notes |
|---|---|---|---|
| Optical | TBD | TBD | TBD |
| Floppy | TBD | TBD | TBD |
| Storage | Internal 3.5-inch hard-drive position | Western Digital Caviar 102AA, WD102AA-53AAA4, 10.2 GB Enhanced IDE | Removed successfully; label photographed and documented |

### Step 4 — Front-Panel Wiring

Before disconnecting:

- [ ] Photograph every connector at the motherboard
- [ ] Record wire colors
- [ ] Record labels
- [ ] Record orientation/polarity where applicable

### Step 5 — Motherboard

**Progress:** Motherboard removed; exact motherboard model remains to be identified from the removed board.

- [x] Photograph board before removal
- [ ] Record mounting-screw locations
- [ ] Disconnect remaining cables
- [x] Remove board
- [x] Photograph exposed motherboard tray and standoffs

### Step 6 — Power Supply

**Progress:** PSU removed from chassis. Factory model label still needs to be documented if accessible on the removed unit.

- [x] Confirm AC cable is disconnected
- [ ] Photograph PSU mounting
- [ ] Record PSU dimensions and label
- [x] Remove PSU without opening its enclosure
- [x] Photograph empty PSU bay

### Step 7 — Drive Cages and Internal Brackets

**Progress:** At least one removable internal drive bracket/cage has been removed and photographed.

- [ ] Determine whether cages are removable
- [x] Photograph attachment points
- [x] Remove selected bracket/cage for survey and access
- [ ] Preserve original hardware

### Step 8 — Empty Chassis Documentation

**Progress:** First empty-chassis photographs captured.

Required photographs:

- [x] Full motherboard tray
- [x] Rear I/O area
- [x] Expansion slots
- [x] PSU bay
- [x] Front interior
- [x] Drive cages
- [x] Rear fan/vent area
- [x] Front intake area
- [ ] Side-panel interior
- [x] Bottom interior


## Drive Bracket / Cage Observation

A removable stamped-steel drive bracket/cage was removed during teardown.

Visible stamped markings indicate support for multiple legacy hard-drive installation positions and orientations. The bracket contains numerous circular and slotted mounting holes and large rectangular access cutouts.

The bracket is being retained because it may be useful for:

- Original-system documentation
- Measuring legacy mounting geometry
- Reuse as a modern 2.5-inch/3.5-inch drive carrier
- Serving as a template for a custom replacement or 3D-printed adapter

No decision has been made yet on whether the original bracket will be reused in the final build.


## Issues Encountered

Record broken clips, seized screws, damaged connectors, proprietary hardware, corrosion, or unexpected chassis construction here.

**None recorded yet.**

## Design Decisions Generated by Teardown

Document any finding that affects the modern build.

**None recorded yet.**

## Next Step

After teardown, complete the chassis measurements in `chassis-survey.md`.
