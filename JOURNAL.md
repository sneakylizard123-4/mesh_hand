---
title: Mesh-Hand
author: sneak
description: Handheld Meshtastic node with on-board GPS, sensors, and a companion app / second revision of a previous handheld board.
created_at: 2026-02-28
---

# 2026-02-28: V1 Kickoff

## What I did

- First commit: started from a backup, initial schematic and PCB, imported E22-900M30S radio and IP5306 battery manager parts.
- Reorganized files into their own folders (kicad/, blender/, images/).
- Wrote the initial README.
- Made a Blender render of the board (Purple.png), took PCB + schematic screenshots.
- Screenshotted the JLCPCB cart / order.

## Why

- Wanted a second revision of my previous handheld meshtastic board.

## Screenshots

![Render](blender/V1/Purple.png)
![PCB](images/V1/old/PCB-old.png)
![Cart](images/V1/2026-02-28-181232_hyprshot.png)

**Total time spent: 5 hours**

---

# 2026-03-01: V1 Schematic Restructure

## What I did

- Reworked the schematic: split the big sheet into `radio.kicad_sch` and `sensor.kicad_sch` and reworked `lipoindicator.kicad_sch`.
- Updated the PCB and fixed silkscreen text clipping.
- Added custom silkscreen footprints (Linux penguin, battery gauge scale).
- Big cleanup pass so routing got easier.

## Why

- (fill in: what motivated the sheet split - too sprawling on one sheet? getting serious about the layout?)

## Screenshots

![Schematic](images/V1/old/2026-03-01-152927_hyprshot.png)
![Schematic](images/V1/old/2026-03-01-201042_hyprshot.png)

**Total time spent: 5 hours**

---

# 2026-03-02: V1 PCB Work

## What I did

- Added more decoupling capacitors (tty7 feedback?).
- Imported 3D packages for the E22 module, NEO-M9N GPS, 901-143 battery holder, and EC11 rotary encoder.
- Updated the PCB.
- Updated the README to follow the blueprint / submission structure.

## Why

- (fill in: why the extra caps, why the 3D models now - render quality / enclosure fit check?)

## Screenshots

![PCB](images/V1/old/2026-03-02-111907_hyprshot.png)
![Layout](images/V1/old/2026-03-02-121155_hyprshot.png)

**Total time spent: 4 hours**

---

# 2026-03-03: V1 Schematics Update

## What I did

- Another schematic pass across all sheets (main, lipoindicator, power, radio, sensor).
- Board got shuffled to match.

## Why

- (fill in)

## Screenshots

![Schematic](images/V1/old/Schematic1.png)

**Total time spent: 3 hours**

---

# 2026-03-05: V1 Board - RTC + Finalized

## What I did

- Worked over two days (03-03 to 03-05 backups show continuous sessions).
- Expanded the sensor sheet, updated board.
- Added the RTC and finalized the PCB.

## Why

- (fill in: why an RTC - timestamping packets, keeping time in sleep/low power?)

## Screenshots

![Schematic](images/V1/old/Schematic2.png)

**Total time spent: 4 hours**

---

# 2026-03-06: V1 Sensors and 1.8V Rail

## What I did

- Big rework of the power sheet: added a 1.8V power supply rail.
- Reworked the sensor sheet and rewired the board.

## Why

- (fill in: what sensor needs 1.8V - measuring the thing, or the MCU IO? what does the 1.8V feed?)

## Screenshots

![Schematic](images/V1/old/Schematic.png)

**Total time spent: 3 hours**

---

# 2026-03-07: V1 More Sensors + 3D Models

## What I did

- Added more sensors with their STEP models: MAX30102 (heart rate / oximetry), SCD41 (CO2), WS2812B-2020 (LED).
- Updated the board, regenerated the gerbers, updated the BOM.
- New Blender render of the fuller board.

## Why

- (fill in: why a CO2 sensor on a portable radio? what do you plan to do with the vitals?)

## Screenshots

![Render](blender/V1/Untitled.png)

**Total time spent: 5 hours**

---

# 2026-03-26: V1 Fab Variants

## What I did

- Generated separate production zips for PCBWay and JLCPCB (`mesh_hand_PCBWAY.zip`, `mesh_hand_JLCPCB.zip`).
- Minor board edit to allow both fabs.

## Why

- (fill in: comparing fab options - JLC local, PCBWay US for tariffs/lead time?)

## Screenshots

![Cart](images/V1/2026-02-28-181307_hyprshot.png)
![Cart](images/V1/2026-02-28-181344_hyprshot.png)

**Total time spent: 3 hours**

---

# 2026-03-27: V1 CAD - STEP Export Fight

## What I did

- Exported the full board to a .step file (huge, 750k lines).
- First model had issues ("fix issues?", "help me"), renamed, then deleted it.
- Re-exported a working `mesh_hand.step`.

## Why

- Required `.step` for the submission and useful for an enclosure fit check.

## Screenshots

![PCB](images/V1/old/2026-03-01-153906_hyprshot.png)
![PCB](images/V1/old/2026-03-01-201056_hyprshot.png)

**Total time spent: 4 hours**

---

# 2026-03-30: V1 Cleanup

## What I did

- Regenerated clean schematic screenshots (Sch1-5.png) + new PCB render.
- Moved the old messy screenshots into images/V1/old/.

## Why

- README and submission need clean, legible images, not random screenshots.

## Screenshots

![Schematic 1](images/V1/Sch1.png)
![Schematic 5](images/V1/Sch5.png)
![PCB](images/V1/PCB.png)

**Total time spent: 3 hours**

---

# 2026-09-06: V2 Start

## What I did

- Reorganized the repo: old work moved under images/V1/ and blender/V1/.
- Started V2: separate sub-sheets for esp32, gps, oled, power, radio, rtc, sensor.
- Imported a different radio (E22-400M33S) and new MCU footprint + 3D models.

## Why

- need 

## Screenshots

![Root](images/V2/01-root.png)
![Power](images/V2/06-power.png)
![ESP32](images/V2/07-esp32.png)

**Total time spent: 4 hours**