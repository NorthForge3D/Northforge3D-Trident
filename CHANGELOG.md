# NorthForge3D Trident — Changelog  
All development updates for the Trident dual-gantry proof-of-concept platform.  
This log documents progress as this machine evolves

## 2025-12-11
---
- Reversed previous decision to separate out mods into separate cad folders
- Renamed one folder to NF3DModdedCad, this will house all mods / changes
- Moved previously designed top frame stiffeners to new CAD file - NF3D-Trident
- CAD directories are now NF3DModdedCad, and Trident-Original-CAD (for reference when needed)
- Work will continue in the one NF3D-Trident file

## 2025-12-09 - Finished design, exported and printed / confirmed corner brakets
---
- Ensured the bolts were inset, M5 bolts inset 4 into 10mm thick brackets
- Exported to STL
- Printed in ABS, and ASA-CF
- Bolted to 2020 extrusions without an upright to ensure - squareness printed on a 2.4 and 0.2 printer .. both work
- Confirmed bracket will hold a corner by itself, and thus, stiffen the blind corners
- Confirmed with machinist square, when printed with a well-tuned machine, these are exactly square. Will help to square the printer rather than work against it. 
- Confirmed stiffness, printed at 5 walls, 5 top and bottom layers, 60% gyroid infill, I cannot feel flex in these pieces.  A vice and a hammer would be required to break them. 
- Stiffness increase confirmed!

## 2025-12-08- Designed Corner Braces for the Top of the Printer
---
- Designed top brackets that will sit at the top of the printer 
- Brackets will be used at all corners around the top of the frame. 
  - 4 brackets around top ring
  - 1 bracket at x and one at y at each corner

## 2025-12-07
---
- Perfected the VR CAD environment, work can now proceed with up to 5 screens as large as needed to see fine details. 

## 2025-12-06 - Added working cad files to the Electronics Bay and Frame Section
---
- Created working CAD files to two directories
  - ElectronicsBay/ working cad file, portions not needed removed
  - Frame/ working cad files, all irrelevant cad removed
- To create CAD for electronics / frame stiffeners / pi through skirt over the coming week

## 2025-12-03 — CAD Restructure & Workflow Stabilization
---
- Significant restructuring of the `/cad` directory to support the Trident proof-of-concept redesign work.
- Created a clean modular layout with the following working directories:
  - `ElectronicsBay/`
  - `Frame/`
  - `Gantry/`
  - `Panels/`
  - `NF3DReassembled/` (full linked assembly)
  - `Trident-Original-Cad/` (reference, untouched)

- Added README.md files to all CAD subsystem folders:
  - Explains purpose, scope, and goals of each subsystem.
  - Documents the workflow for modifying vs. referencing CAD.

- Defined the CAD development workflow:
  - Work exclusively inside subsystem directories (Frame, Panels, Gantry, ElectronicsBay).
  - Keep `Trident-Original-Cad/` as a pristine measurement and comparison reference.
  - `NF3DReassembled/` acts as the main assembly for validating alignment, clearances, and interference.

- Simplified the versioning strategy:
  - V0 *is* the physical build unless a major design flaw appears.
  - No V1/V2 iterative CAD folders needed.
  - The Deuce will be a completely new CAD project based on learnings from this proof-of-concept.

- Removed unnecessary directory complexity in favour of a fast, focused workflow optimized for working in VR and performing subsystem-level edits.

- This completes the foundational CAD structure required to begin focused engineering work on:
  - Frame stiffeners  
  - Electronics bay redesign  
  - Panel system modifications  
  - Dual-gantry integration

- Tonight’s work stabilizes the NF3D CAD process and prepares the project for accelerated development as parts begin arriving in December.
\
e

## 2025-11-26
---
 - Added to BOM 
  - decided on a build volume of 250mm x 250mm x 200mm for the first build
  - shortened Z height and smaller bed frame are good for our first - STIFF - trident
  - ordered raw 2020 extrusions, psu, ssr, buck converter (adjustable with display for experiamental build), all rails mgn 9 and 12, terminal stripes for clean wiring with a dual -voltage system. 

## 2025-11-25 - Began CAD work for the NF3D trident mods
--- 
  - Began CAD work on the trident mods
    - Began to create brackets for the bottom rails of the printer
    - A bolt through bracket at each corner, preferably printed from CF-ASA or equivalent, increases rigidity at the corners
    - Leads to design decisions [See DESIGN-NOTES.md → Z Motor Corner Stiffeners](./DESIGN-NOTES.md#2025-11-24--z-motor-corner-stiffeners)

  - Design Choices
    - Decided to use zruncho3d dualing X files as a basis for dual gantry on this printer
      - Is verify on the duelling zero
      - Works
      - Probably needs CAD work to 
      - Gives a basis for klipper files that work 
          - likely need a lot of work to perfect
      - Leads to [See DESIGN-NOTES.md → Gantry Starting Point](./DESIGN-NOTES.md#2025-11-24--gantry-staring-point)

  - Decided on: 
    1. To upload each trident mod as it becomes complete. In it's own NF3D-Added-Parts folder. 
    2. To keep the complete CAD out of the project until each part is printed, validated and tested on the final build. 
    3. With final build / verification - upload complete CAD

## 2025-11-24 - Ordered the majority of the electronics components

## Changelog Entry — Electronics, Lighting, Camera, Motors & CNC Tap (Premium Build Spec) - Ordered

### Order Batch: Electronics + Lighting + Camera + Motors + RGB + CNC Tap
### Date: 2025-Nov-23
---

## 🔧 Main Controller & Motion Electronics
- BIGTREETECH Octopus Pro V1.1 (H723 MCU)
- 8× TMC5160T Pro stepper drivers
- RJ11 → CAN cable (Octopus → UTC)

---

## 🔗 CAN Bus Toolheads & Hub
- 2× BTT EBB36 CAN V1.2 (G0B1)  
  - With ADXL345 accelerometers  
- 2× BTT UTC V2.1 (Triple CAN Output)

---

## 🎯 Probing & Filament Sensors
- **CNC Lab CNC Voron Tap V2** (CNC-machined Tap upgrade)
- 2× SFS V2 Smart Filament Sensors

---

## ⚙️ Custom Motors (NF3D Specification)
- Custom Hanspose NEMA 17 – 42×48mm – 0.9°
- 3× Hanspose NEMA 17 – 42×48mm – 0.9° with integrated 250mm T8×2×1-start lead screws
- 2× Hanspose 36mm Pancake Motors – 0.9° (extruders)

---

## 🧠 Host Controller
- Raspberry Pi 4 – 4GB

---

## 🖥 Display / UI
- Elecrow 5" HDMI Touchscreen  
  - USB-powered (via Pi)  
  - External plug-in design (skirt passthrough)

---

## 💡 Lighting
### Chamber Lighting
- EMITEVER 24V COB LED Strip – 5000K, Ra95+, IP30 (16.4 ft)

### Toolhead RGB
- 2× 5-LED circular RGB boards (behind clear NF3D logo windows)  
  - Driven from EBB36 RGB headers

---

## 📷 Camera (No USB Ports Used)
- Arducam OV5647 – 5MP CSI Camera Module
- Long CSI ribbon cable (gantry-close mounting)

---

## 🧩 Build Notes (Premium Prototype Configuration)
- CNC Lab CNC Voron Tap V2/V1 added for maximum probing rigidity and repeatability
- Dual CAN toolheads using EBB36 boards  
- Dual UTC hubs for flexible CAN topology  
- Pi 4 selected for clean USB-powered display and simpler power routing  
- High-CRI COB chamber lighting + RGB logo lighting  
- CSI camera to preserve USB ports  
- Custom Hanspose 0.9° motion system  
- Integrated Z lead screw motors for premium Z-axis performance  
- This configuration is intentionally beyond kit-grade — this is the **NF3D flagship prototype**.

---

## 📝 Still To Select / Order
### Power System
- 48V PSU  
- 24V PSU or 48→24V converter  
- Optional 5V buck converter  

### Hotend System
- Hotends (Rapido, Revo HF/RF, Dragon HF, etc.)
- Nozzles (hardened + high-flow)
- Heaters (24V or 48V)
- Thermistors or PT100/PT1000

- Bed heater

### Cooling
- 24V toolhead fans  
- 24V part cooling fans  
- 24V chamber fans  
- Optional bed fans  
- Optional filtration system  

---

## 2025-11-23 — Repository Structure Stabilized

- Created first complete folder structure for CAD, docs, and testing workflows
- Added folder-level README files for:
  - `/CAD`
  - `/CAD/NF3D-Added-Parts`
  - `/CAD/Experimental`
  - `/CAD/Trident-Base-Files`
  - `/docs`
  - `/tests`
- Established the CAD-first workflow for all future Trident and Deuce development
- Finalized TODO.md structure to guide Week 1–3 engineering tasks
- Prepared repository for incoming gantry CAD work next week


---

## 2025-11-23 — Repository Cleanup & Folder Structure Planning
- Preparing a proper NF3D-specific CAD folder structure  
  - `CAD/NF3D-Added-Parts/` (gantry components, brackets, plates, etc.)  
  - `CAD/Trident-Base-Files/` (clean separation from Voron origins)  
  - `CAD/Experimental/` (motion system experiments & early prototypes)  
  - `docs/` (mechanical notes, images, and system design references)  
  - `tests/` (gcode, STL validations, and print test data)  
- Beginning to organize Fusion 360 workflows to align with the new directory layout  
- README rewritten to match updated homepage tone & direction  
- Plans established for documenting each NF3D part with notes and revision history  
- Preparing to record the first short YouTube channel intro for the Trident project

---

## 2025-11-19 — CAD Workflow Transition
- Removed Trident-specific STLs, drawings, and manuals  
- Transitioned to a **CAD-only workflow** to allow rapid iteration  
- Began preparing custom modifications for dual-gantry testing  
- Established rule: **STLs added only after printed and validated**  
- Planning early development logs (Week #1)  
- Next major update planned for late November — aligns with arrival of custom 0.9° motors

---

## 2025-11-14 to 2025-11-18 — Early Repository Setup
- Initial repository created for Trident-based dual-gantry proof-of-concept  
- Began removing Voron-specific logic and preparing for NF3D divergence  
- Early experiments with toolhead routing, gantry plates, and belt layouts  
- Established the principle: **open development first, refinement later**

---

## 2025-11-01 — Project Direction Set
- Defined Trident POC as the foundation for validating:  
  - Dual-gantry motion  
  - Toolhead choreography  
  - Collision-avoidance logic  
  - High-precision motion using 0.9° steppers  
- Identified need for clean, service-friendly electronics layout  
- Decided on inverted-electronics concept for visibility during testing  
- Began planning the Deuce’s architecture at the high level

---
