# CHANGELOG

The changelog records **what changed and when** as the project progresses.

This file focuses on concrete actions: CAD work completed, parts created or modified, files added or removed, and decisions that materially affected the state of the project. Entries are chronological and factual by design.

When important design rationale, tradeoffs, or forward-looking thinking influenced a change, those details are captured in **DESIGN-NOTES.md**, and entries here link back to the corresponding design notes where appropriate.

Together:
- **CHANGELOG.md** documents *what was done*
- **DESIGN-NOTES.md** explains *why it was done*

Both are maintained intentionally to preserve context, trace decisions, and make the project understandable to future contributors, builders, or reviewers.

## 2026-01-07 — Skirt Work

- Continued work on the skirt system
  - Began designing a **three-piece, between-the-corners skirt system**
    - Once a single block is finalized, skirts can be printed in that form
    - Three skirt pieces between each corner block
    - Planned variants:
      - Pi passthrough section
      - AC inlet / switch section
      - Screen mount section
    - Current design targets **300 mm build size only**
    - All pieces:
      - Friction-fit using designed tabs
      - Bolt to the bottom frame
      - Bolt into the corner blocks
      - Considering a simple one- or two-bolt skirt-to-skirt connection using heat-set inserts to reduce flex and prevent the skirt from feeling flimsy when lifting the printer

  - Corner block (blank version) is printing to validate:
    - Overall size and proportions
    - Bulk vs. stiffness balance
    - Intended to add bottom-frame stiffness without excessive bulk
    - Design can still be easily adjusted before completing the remaining skirt components


## 2026-01-06 — Updates / Videos

- Continued work on printer skirt design
  - Switched to a modular skirt system
  - Corner pieces completed; designed to add stiffness at the lower frame
  - Side skirts designed as interchangeable modules
    - Three repeatable sections between each corner
    - Center section can be swapped (e.g. no screen, alternate panel)
    - Front pass-through ports can be relocated by swapping modules
    - All skirt modules interface identically for flexible configuration

- Cut the printer frame extrusions
  - Tapping, drilling, and final prep still pending

- Started a new YouTube series: *How to Build Your Own 3D Printer Frame*
  - Intro video published explaining how to derive frame dimensions from the Voron BOM
  - Playlist created to document the full cut / drill / tap / assembly process
  - Video: https://www.youtube.com/watch?v=7mM1ULKVuBA


## 2026-01-04 — Frame cut, STL folder added

### Frame Preparation
- Cut all aluminum frame extrusions to final size.
  - Frame geometry remains identical to the original Voron Trident.
  - Overall height reduced by **50 mm** for this build.
  - Used **vorondesign.com** to derive the full cut list from Misumi part numbers.
  - All 2020 extrusions cut to length.

### Jigs & Tooling
- Designed custom CAD drilling jigs for:
  - Blind corner holes
  - Gantry mounting holes at precise offsets from the top of the frame
- Printed all required drilling jigs.

### Repository Structure
- Added `STL/` folder to the repository.
  - This directory will house all validated and tested STL files.
  - Current structure:
    - `STL/Frame/` — frame stiffener parts
    - `STL/Tools/` — drilling and alignment jigs
  - Added README files to `STL/` and all subdirectories.

### Documentation & Media
- No updates to `DESIGN-NOTES.md` tonight.
  - Frame design rationale was fully captured in the previous entry.
- Recorded a video documenting the 2020 extrusion cutting process.
  - Video will be published to the YouTube channel tomorrow or the following day.


## 2025-01-03
*(Related entry: [DESIGN-NOTES.md — 2025-01-03](DESIGN-NOTES.md#2025-01-03---slow-progress-ideas-coming-together))*

- Continued work on redesigned skirts.
  - Corner blocks will be similar in concept to the **top frame stiffeners**.
    - Extend **60mm outward** from each corner.
    - Include **two M5 bolts into T-nuts** per rail (4 total) to clamp the frame tightly.
    - Each corner includes an interface to accept the next rail section.

  - Skirt pieces will bolt **to each other** and **to the frame** for added rigidity.

  - Bottom of skirts includes a **5mm inset**.
    - Electronics panel will sit inside this inset.
    - On the first printer, this panel will be made from **1/4\" Lexan**.

  - Electronics panel mounting strategy:
    - Panel is held upward into the skirts using brackets.
    - Two brackets per side, plus additional attachment near the corner feet.

  - Corner feet design:
    - ABS bracket bolted into the corner to support the electronics panel.
    - TPU foot approximately **10mm thick** for vibration isolation and grip.

- See corresponding **design rationale and planning notes** in the linked Design Notes entry above.


## 2025-12-28 – Skirts and Electronics

- See related design thoughts in  
  → [DESIGN-NOTES.md · 2025-12-28 – Design Decisions, Skirts, Electronics](DESIGN-NOTES.md#2025-12-28--design-decisions-skirts-electronics)

- Started working on new skirts for inverted electronics and pass-through Pi
  - Imported Trident skirts and separated out the pieces I will and won’t use
  - Corner pieces are usable as-is
  - Identified required changes:
    - New front skirt to support an **external-mounted screen** (optional, not required for base build)
    - Right-side skirt redesigned for **USB / Pi pass-through**
    - Rear skirt redesigned for an **all-in-one module** (AC inlet + rocker switch)

- Imported most electronics components into CAD:
  - Mean Well LRS-350-48
  - Mean Well RS-25-5
  - 48V → 24V buck converter
  - SSR and related hardware

- Began printing frame stiffeners and gantry parts for visualization and fit testing



## 2025-12-27 - Working on Gantry Parts, Electronics

- See related design thoughts in **[DESIGN-NOTES.md — 2025-12-27](DESIGN-NOTES.md#2025-12-27---gantry-thoughts-bed-move)**

- Started working on flipping the gantry for side-to-side dual gantry
  - Drilled new holes and moved the gantry rails to the front and back
  - Identified multiple issues that will need to be addressed for this approach to work:
    - Bed will need to be moved further back (more centralized in the frame)
    - Rear Z MGN rail / support will need to be moved inward or
      an additional rear frame crosspiece added below the rear gantry rail
    - In practice, **both changes will likely be required** — see Design Notes

- Started printing test pieces
  - Standard Trident A/B motor mounts and idler mounts
  - ZRunchoes dual-gantry-related parts (Trident-sized variants)
  - Building a physical test gantry to visualize layouts and interference
  - Goal is to validate clearances, belt routing, and mounting before final CAD
  - Enables rapid iteration: parts can be installed, evaluated, or discarded quickly

- Began simplifying CAD models for electronics
  - Example: Octopus Pro now represented as a dimensionally correct simplified model
  - Color and envelope preserved for electronics bay layout
  - Detailed board CAD removed where not needed

- No CAD commits made yet
  - Will commit once electronics bay and skirts are finalized
  - Gantry and Z-axis modifications will be committed separately once resolved
 



## 2025-12-21 – Motion Rails and Electronics Kit (CAD)
↔ See related design thoughts in [DESIGN-NOTES.md – 2025-12-21](DESIGN-NOTES.md#2025-12-21---design-thoughts---cad-and-control-systems)

- Began creating the foundations of the motion system to allow the gantry to be expanded to the newly defined, properly sized frame.
  - Created **MGN9 rails and MGN9H blocks** in CAD.
    - Fully parametric
    - Assembled with proper motion constraints (blocks slide on rails)
  - Created **MGN12 rails and MGN12H blocks** in CAD.
    - Fully parametric
    - Assembled with proper motion constraints
- Began locating and importing representative electronics components for the electronics bar:
  - **BTT Octopus Pro v1.1** imported and positioned in CAD
  - **Raspberry Pi 4** imported and positioned in CAD
  - **Two representative power supplies** imported and positioned in CAD
- CAD was **not committed** today.
  - No meaningful architectural changes were made
  - This work focused on creating prerequisite parts required for the next design step
- Design rationale and system-level thinking captured in **DESIGN-NOTES.md**


## 2025-12-19 – Expand Exterior Frame in CAD

- Working in the new CAD, expanded the exterior frame to proper dimensions for a 300 × 300 × 250 build volume
- Exterior frame is now correctly sized at **460 × 460 × 500 (H)**
- All frame joints are now rigid, making this a true structural frame rather than loose extrusions
- Electronics planning update:
  - Ordered DIN rails, terminal distribution blocks, and DIN-mounted AC and DC fuse holders
  - This will allow for a much cleaner, more serviceable, and showpiece-level electronics bay

**Next steps:**
- Expand remaining aluminum frame components
- Expand and place the gantry
- See **[DESIGN-NOTES.md → 2025-12-19 – Gantry Design Thoughts](DESIGN-NOTES.md#2025-12-19--gantry-design-thoughts)**



## 2025-12-18
---
- Moved the frame, gantry, and electronics into a new CAD file:  
  **NF3D-Frame-Electronics-Gantry.f3D**
- Removed all parts not required for this portion of the CAD
  - Work will now focus only on the larger structural and system-level modifications
  - Electronics were intentionally kept and will be flipped, repositioned, and reorganized
  - New skirts will be designed to support:
    - An inset bottom panel
    - Support for 2–3 DIN rails
    - A Pi pass-through design to allow USB / HDMI access from outside the printer
- Updated **DESIGN-NOTES.md** with rationale and design decisions  
  → See: **[2025-12-18 – New CAD and Decisions](DESIGN-NOTES.md#2025-12-18---new-cad-and-decisions)**


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
  - Electronics will likely be **inverted-facing** for aesthetics, but must remain serviceable
  - This orientation is required for the first build and may become permanent
- **Concept not committed**:
  - Current design needs refinement
  - Must provide real frame stiffening — **accomplished**
  - Must function as a simple panel mounting system — **accomplished, but needs refinement**
  - Must **not interfere with existing Voron Z-motor mounting** (no redesign justified)
- Deck panel design must remain **simple to manufacture** (easy to cut; no unnecessary complexity)


## 2025-12-14

- Watching back the YouTube video: brackets printed on the Sovol show visible shift artifacts. Parts are still square, but for example/validation pieces, slow the printer down or use the Vorons. ABS prints benefit from lower speeds for both strength and dimensional precision. Note for future part confirmations and videos.
- Watching video back: it may be useful to record two points of view at once. Record my face and talking while recording my hands working. Easy way to do this, without compromising "I am not a youtuber, I have no intention of spending money on recording equiptment" .. Use the macbook to reocrd me, use the iphone and the $20 arm I bought to record me working. This will be useful in future videos when we're building a large frame, etc. As I can switch views. This adds 3 minutes of video editing time...

## 2025-12-11

- Reversal of original CAD separation. All CAD now housed in the NF3D-Trident file. This will improved work flow.
- Turned 1 bracket into 12 around the top. Loosely (messy cad) placed them until I add the t-nuts, and the m5 bolts.
- With the shortened printer, this stiffener design will work. If I built it taller, may need to consider weight. How much does 48 M5 bolts and 48 t-nuts add in weight?
- This is the design for this shortened dual grantry trident, may reconsider the number of braces if we decide to release this printer in kit form. If I stiffen significantly (I have) but add a 0.5 - 0.8kg of weight at the top, I may reduce movement at the joints but increase the wobble in the aluminum itself. Will try to calculate based on X height vs, X weight at the top frame. Added stiffness is still more important for this first printer. Build volume is shorter, movement at the top is already reduced. Stiffening it will reduce it further over the length of upright we will be using.

## 2025-12-09 Top Frame Stiffeners Created in Cad, Validated by Printing

- 10mm x 20mm x 60mm corner brackets designed yesterday, 2 bolts per rail into t nuts
- Tried to keep the asthetics of the printer correct
- Will use these brackets around the top frame, and also once confirmed non-interference, at each corner of the X/Y around the top
- We have decided to build with a volume of 300x 300y 200z ... shortening this printer will further stiffen the frame. 48V rail moving two print heads as quickly as we can without smashing into each other (hopefully) will require every bit of stiffnes
