# NorthForge3D Trident — Changelog  
All development updates for the Trident dual-gantry proof-of-concept platform.  
This log documents progress as this machine evolves

## 2025-12-17
---

- Redesigned and modified the **bottom front brackets**.  
  - They now function as **frame stiffeners** and **bottom clear panel holders**.  
  - Interface cleanly with **VORON motor mounts**.  
  - Will print and physically validate this weekend.

- Added **frame stiffeners along the rear X/Y** by duplicating the top bracket design.

- Decided **no additional stiffening is required on the bottom**.  
  - Skirts, motor mounts, and existing structure already contribute sufficient rigidity.

- Ready to move on to **Electronics Bay / Skirts**, followed by a **working CAD gantry**.

- Downloaded CAD for the **electronics boards selected for the first build**.

- Added a detailed entry to **DESIGN-NOTES.md** covering current CAD, build, and kit-planning decisions:  
  → [2025-12-17 – CAD Design & Build Decisions](./DESIGN-NOTES.md#2025-12-17---cad-design--build-decisions)

## 2025-12-16
---

- Designed initial **bottom frame stiffeners** intended to both increase frame rigidity and act as a **drop-in deck panel support**
- Defined deck panel requirements:
  - Must be **easily removable** for electronics access
  - Should **drop in** and allow **lift / flip-up access**
  - Electronics will be **inverted** for aesthetics, but must remain serviceable
  - This orientation is required for the first build and may become permanent
- **Concept not committed**:
  - Current design needs refinement
  - Must provide real frame stiffening- accomplished
  - Must function as a simple panel mounting system - accomplished but needs refinement
  - Must **not interfere with existing Voron Z-motor mounting** (no redesign justified)
- Deck panel design must remain **simple to manufacture** (easy to cut; no unnecessary complexity)

## 2025-12-14
---

- Printed several top frame brackets.
- Confirmed ASA-CF bracket strength by hand testing. Bracket could not be broken by hand; failure was only possible when mounted without an upright, which exceeds expected use. Strength confirmed sufficient for intended stiffness role.
- Printed 2020 extrusions out of black abs, created blind corners with it
- Inserted brackets into extrusions, confirmed strong with all plastic
- Confirmed brackets print square (within machinist square tolerance) on one Voron and one Sovol printer.3
- Recorded YouTube video of the brackets and explaining their purpose: https://youtu.be/TB5Z2YtNPzY?si=88zf4GWxYT6D0n6M
- Created blog post with video, and text explanation: https://northforge3d.com/forge-updates/trident-build/frame-stiffness-matters-controlling-compliance-racking-and-micro-slip-in-a-dual-gantry-printer/
- Worked in CAD to place all 12 brackets in place using rigid joints
- Confirmed non-interference in CAD
- Turned NF3D mods, green. This will help to distiguish Trident CAD from our CAD as we move forward
- Updated Repo

## 2025-12-11 - 2 - Duplicated Brackets for Top Brace
---

- Created copies of the original bracket design
- Rotated and poorly placed them
- Still need to add T-Nuts, joints in CAD and M5 x 12mm bolts
- Adds - 48 M5 bolts, 48 t-nuts at top frame .. necessary for this iteration

## 2025-12-11 - Reversed previous bad decision of splitting CAD files into folders
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
- Confirmed stiffness, printed at 5 walls, 5 top and bottom layers, 60% gyroid infill, I cannot feel flex in these pieces. A vice and a hammer would be required to break them.
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
  - Frame stif
