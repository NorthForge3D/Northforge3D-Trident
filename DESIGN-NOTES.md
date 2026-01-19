# DESIGN NOTES

Design Notes exist to capture **why** decisions were made, not just **what** was done.

While `CHANGELOG.md` records concrete actions and visible progress, this file documents the reasoning, tradeoffs, constraints, and forward-looking thoughts that led to those actions. Together, they form a linked record:

- **CHANGELOG.md** → what was built, changed, or tested  
- **DESIGN-NOTES.md** → why those choices were made, and what alternatives were considered

Entries here may include incomplete ideas, exploratory thinking, or decisions that evolve over time. That is intentional. This file is a living design journal meant to provide context for future work, explain past decisions to collaborators or builders, and make the project’s direction understandable long after individual commits are forgotten.

## 2025-01-18 — Logos Added to Corner Skirt Pieces

- Brief hiatus to repair a required printer for this project (lost ~1 week)
  - Burned out a control board (operator error)
    - Replaced with an MKS SKIPR
    - Not documented well / at all for this printer
      - Made configs from scratch - took time. 
  - Goal is to print the first modified bed mounts in PAHT-CF
  - Need to better understand annealing shrinkage/contraction so it can be accounted for in CAD
  - Voron 0.2 is operational again
    - Swapped extruder motor to 0.9° stepper
    - Retained Dragonfly BMO hotend and RepRap nozzle
    - Currently printing very well with ASA-GF

- Added Voron logo cutout to the left front corner skirt block
  - Includes a separate insert intended to be printed in translucent filament and backlit

- Added NF3D forge icon to the right front corner skirt block
  - Includes a separate insert intended to be printed in translucent filament and backlit

- Voron version currently printing to confirm part


## 2025-01-08 — Skirt / Corner Block Thoughts

- Printed the first corner block to confirm the STL
  - Part is confirmed
  - Slight design changes are needed to make it printable by less-capable printers

- Venting considerations:
  - Venting at the corners likely isn’t necessary
  - Venting through the skirts isn’t necessary on this printer
  - The printer has active fans to move air
  - Electronics bay is inverted and a good distance from the heated bed
  - Three fans are planned
  - Skirts are modular — others can add more fans if they choose

- Design changes:
  - Add chamfers and an inset panel to make corner blocks more printable
  - Add logos to the front corner blocks
    - NF3D logo on one side
    - Voron logo on the other
    - I’m changing a lot — it’s my printer now — but it started as a Trident and will remain the NF3D Trident

- Content / documentation:
  - Reviewed Part 2 in the **How to Build a 3D Printer Frame** playlist
  - Added a blog post to more clearly explain the cutting process
  - Linked the article at the top of the video description:  
    http://northforge3d.com/forge-updates/3d-printing-tutorials/how-to-cut-2020-aluminum-extrusion-for-a-3d-printer-frame/

- Hardware notes:
  - May need to bring one of the larger Vorons home from the shop
    - The Voron 0.2 isn’t large enough for some upcoming parts
    - The SOVOL experienced a clog
      - Reinstalled the MicroSwiss hotend
      - Ordered additional 0.4 mm hardened nozzles (arriving Monday)
      - Ordered an additional MicroSwiss hotend with 0.6 mm and 0.4 mm hardened nozzles
      - Original MicroSwiss hotend is likely approaching 600–800 hours

- Summary entry for this work is recorded in  
  [CHANGELOG.md — 2026-01-08](CHANGELOG.md#2026-01-08--confirming--unconfirming-parts--cut-video-posted)




## 2025-01-03 - Slow progress, ideas coming together
*(Related entry: [CHANGELOG.md — 2025-01-03](CHANGELOG.md#2025-01-03))*

- Spent the past couple of evenings working on skirts.
  - Finalized the electronics bay concept: a single removable panel with **three DIN rails**.
    - DIN rails are bolted to the panel via an **ABS interface**, holding the rails **15mm off the panel** to allow wire routing underneath.
    - Printed wiring channels between DIN rails, evenly spaced at **three locations** (front, middle, back).
      - Channels are printed in ABS and include pass-through ports for clean wire entry and exit.

- Corner skirts are intended to **add structural rigidity** to the frame — stiffer is better for this printer.
  - Design is still in progress for all skirt components and will be uploaded once complete.

- Set up the saw with the correct **aluminum-specific blade** and added a clamping system for accurate, repeatable cuts.
  - This portion of the build could be completed at the shop, but I cannot record anything there.
    - Documenting processes like *cutting extrusions*, *tapping extrusions*, and *drilling blind corners* will still be valuable to the community,
      even if kit builders won’t need to perform these steps themselves.

- Started printing gantry parts (A/B drives, etc.).
  - **Estimated timelines:**
    - CAD completion for skirts and electronics bay: **~1 week**
    - First frame build / test frame for gantry parts: **~1 week**
    - After that, we can build, test, and redesign specific **dual-gantry drive systems** on a physical frame.



## 2025-12-28 – Design Decisions, Skirts, Electronics

- After reviewing the current CAD more closely yesterday, I decided to **build the frame early**
  for the test gantries and iterate the design around a physical reference.
  - Ordered a new aluminum-specific mitre saw blade (old one was worn out; not available locally)
  - Ordered an additional M6 tap for European-spec 2020 extrusions

- Worked on CAD for skirts and the electronics bay
  - Most skirts need modification so the **bottom panel seats into them** rather than bolting up to them
  - Skirts must support **DIN rails** (three for this build) to keep wiring clean and visually organized
  - Electronics cooling plan:
    - Two intake fans (left and right) pulling in cooler room-temperature air
    - One exhaust fan at the rear expelling warmer air
  - Required skirt redesigns:
    - One side skirt for **Pi pass-through**
    - Left rear skirt for the **clip-in AC inlet / switch module** already on hand
    - Center front skirt redesigned to include a **screen interface module**
      - Screen will be optional and externally mounted
      - Simple mechanical interface so the printed screen enclosure clips into place
      - Possibly secured from the inside with fasteners

- Started printing parts for **test gantry one and two**
- Also began printing parts for the actual Trident build
  - A/B brackets
  - Idler pulley brackets
  - Having a real frame to work against will greatly improve visualization and iteration speed

- Frame build documentation plan:
  - Capture and record useful processes for other builders:
    - Cutting aluminum extrusion
    - Drilling for blind corners
    - Tapping techniques
    - General frame prep and accuracy tips (Squaring,etc )
- Related build progress logged in  
  → [CHANGELOG.md · 2025-12-28 – Skirts and Electronics](CHANGELOG.md#2025-12-28--skirts-and-electronics)

## 2025-12-27 - Gantry Thoughts, Bed Move

> Related work logged in **[CHANGELOG.md — 2025-12-27](CHANGELOG.md#2025-12-27---working-on-gantry-parts-electronics)**

- While working on flipping the gantry rails for a side-to-side dual gantry layout,
  two major constraints became immediately apparent:

  - **Bed placement**
    - The bed is currently too far forward on the Trident frame
    - For a dual gantry setup, the bed will need to move inward (more centralized)
    - This will require redesigned bed mounts specific to this build

  - **Rear Z rail / support structure**
    - The current rear Z MGN rail and support design will not work as-is
      for a side-to-side gantry configuration
    - Several possible approaches to address this:
      - Flip bed motors side-to-side and add an additional frame crosspiece
        to support the single now side mounted motor
      - Redesign gantry mounts so the gantries ride on MGN9 rails mounted
        on top of the 2020 extrusion instead of hanging below
      - Do not flip the gantry at all:
        - Keep the bed centralized
        - Allow printheads to approach from front and back
        - Likely the simplest solution, but **no commitment yet**

- Began printing parts for a physical test gantry
  - Original Trident A/B motor, pulley, and idler components
  - ZRunchoes Trident-sized dual gantry parts
    - These parts were designed for a different class of printer
    - As far as I know, they have not been implemented on a Trident
      despite being made parametric/resizable

- Purpose of the test gantry
  - Allows direct visualization of clearances and interference
  - Enables testing belt routing, pulley placement, and gantry spacing
  - Confirms feasibility before motors or final CAD are locked in
  - Supports rapid iteration without risking the primary frame

- Initial assessment
  - There is still a strong possibility that the original Trident
    A/B motor and pulley mounts can be retained
  - Idlers will need to be relocated
  - Physical assembly will determine whether this remains viable



## 2025-12-21 – Design Thoughts – CAD and Control Systems
↔ See related implementation work in [CHANGELOG.md – 2025-12-21](CHANGELOG.md#2025-12-21--motion-rails-and-electronics-kit-cad)

- Created motion rails in CAD and made them fully parametric so rail length can be adjusted easily while preserving motion constraints.
- No need to commit CAD on days like this.
  - Built supporting components
  - Imported reference electronics
  - No meaningful structural changes were made to CAD that lives in the repo
  - These are preparatory pieces required to continue design work cleanly
- For some imported CAD components, the models will need to be simplified.
  - Example: the **Biqu Octopus CAD** is a full, component-level electronics model
  - I do not need resistor-, IC-, or component-level detail
  - I only need:
    - Dimensionally accurate representations
    - Correct mounting geometry
    - Visual references for DIN rail placement and clearances
  - I am not wiring electronics in CAD
- Could not find CAD for the exact planned power supplies.
  - Used manufacturer dimensions to import a **Mean Well PSU** with closely matching dimensions
  - Dimensional accuracy matters for DIN rail mounts and placement
  - The full electronic detail does not matter here

- Spent time evaluating the current state of **Klipper and its forks**.
  - Thinking through how this system will ultimately work:
    - Two print heads “dancing”
    - Two heads printing a single part
    - Guaranteed non-collision behavior
  - May use **Kalico** for the first printer.
    - I believe I can demonstrate the concept largely through configs and macros
    - I built it, I understand it, and I won’t break it
  - Before releasing this as a kit—or releasing **The Deuce** as a production unit—I may need to fork **Klipper or Kalico**.
    - Collision avoidance for a dual-gantry system must live in the motion control software itself
    - It cannot live in:
      - G-code
      - The slicer
      - Config-only logic
    - A kit that relies solely on configuration-based collision avoidance will eventually be broken by users modifying configs
    - That results in broken machines
  - **The Deuce** is intended to be:
    - Expandable
    - Serviceable
    - Reliable
  - If adding or modifying a component can break the machine due to a configuration mistake, that is unacceptable
  - This will need to be revisited as we move through:
    - Mirror mode
    - Independent dual-head printing
    - Dual-color modes
    - Dual-material modes
  - A decision will need to be made, and the safest long-term solution for a kit or production machine is to make collision avoidance part of the system that directly drives the motors

## 2025-12-19 – Gantry Design Thoughts

- Frame expansion is complete.
- Next step is to expand, flip, and install the gantry correctly in CAD.

- The Trident gantry is currently linked as one solid piece.
  - It will need to be broken apart so individual components can be positioned correctly.
  - Single parts must be moved into place to create a proper, functioning motion system.

- For portions of the gantry work, it may be easier to source working CAD rather than fight what currently exists.
  - Example: MGN rails and blocks.
    - These must behave correctly in CAD.
    - I need to be able to grab a carriage block and have it move accurately along the rail.
    - Eventually, I should be able to grab a printhead and move it in CAD.
    - Belts, pulleys, and idlers must respond correctly so the full motion system is represented accurately.

- There is no reason to redesign Trident gantry mounts.
  - The design already works and is proven.
  - The task is to disassemble the existing CAD assembly and reassemble it piece-by-piece on the expanded gantry rails.
  - This includes adding correct motion behavior to idler pulleys, timing pulleys, and bearings.

- All of this work is necessary to properly prove the gantry and motion system in CAD before moving forward.

(See **[CHANGELOG.md → 2025-12-19 – Expand Exterior Frame in CAD](CHANGELOG.md#2025-12-19--expand-exterior-frame-in-cad)**)




## 2025-12-18 – New CAD and Decisions

- The Trident is built very bed-forward, so the gantry will need to be rotated sideways.
- This orientation reduces X/Y volume loss.  
  If a second gantry were added in the same orientation, we would lose:
  - The depth of the gantry rail
  - The printhead offset
  - Additional space for belts and the X pulley system
- Rotating the gantry preserves more usable X/Y volume and simplifies future expansion.

- Decided to use switching power supplies for this build.
  - Ordered **two 500W, 0–60V Hongpoe PSUs**
  - These are not as trustworthy as Mean Well units, but with a 4.8 rating and 300+ reviews on AliExpress, they should be sufficient for testing and development
  - Voltages will be tested and verified before connecting to any control boards

- Using switching PSUs allows flexibility as the system evolves:
  - Start with a standard 24V Klipper configuration using dual PSUs
  - Transition to 48V on the X/Y/Z rails once the dual gantry is printing reliably
  - Voltage headroom exists to go higher (up to ~56V if ever needed)
    - Not currently required, but the option exists
    - Control boards and drivers are capable of handling 60V max

### Why This (NEW CAD) Matters

- Creating a dedicated frame / gantry / electronics CAD allows the project to move to a **true 300 × 300 × 250 build volume**, instead of being constrained by the original Trident 250 × 250 × 250 layout.
- Working at the correct size enables:
  - Proper electronics layout at full scale
  - Skirts designed to the final footprint
  - Accurate DIN rail placement and power distribution planning
- This file also allows the **dual-gantry system to be designed and validated as a movable, working assembly** in CAD, at the correct size, before any physical assembly begins.
- Resizing and reworking the original Trident CAD would be slow and inefficient:
  - The file contains 300+ parts
  - Rescaling the frame, flipping X rails, reworking the gantry, and adding a second gantry would take 1–2 days just to reach a usable state
- Starting fresh with a purpose-built CAD significantly reduces friction:
  - Frame resize, electronics flip, and DIN-based layout can be completed in 2–4 days
  - Motion systems can be developed and tested in isolation without fighting the full Trident assembly
- Working in a smaller, focused CAD eliminates constant hide/show management of dozens of unrelated components, allowing faster iteration and clearer decision-making.
- This approach trades sentimental continuity for **speed, correctness, and forward momentum**, which is critical at this stage of the project.

→ Related log entry: **[CHANGELOG – 2025-12-18](CHANGELOG.md#2025-12-18)**

## 2025-12-17 – CAD Design & Build Decisions

- For the electronics bay, it will be simpler and cleaner to work from a **separate CAD file**.
  - This file will include the **full frame** and all **relevant structural reference parts**.
  - It will be expanded to the **standard build volume of 300 × 300 × 250**.

- This approach allows:
  - A **single source of truth** for skirts, electronics bay, gantry, and panels.
  - All parts to be designed together so **everything fits correctly by default**.
  - Accurate, repeatable dimensions that can be provided directly to suppliers if we decide to offer this printer as a **build kit**
    (e.g. *cut to this length, drill here*).

- The gantry CAD will be designed **with motion constraints**, allowing motion to be tested in CAD before committing parts to a physical printer.

- I may build this printer **twice**, in parallel, specifically for video documentation.
  - I already have enough extrusion to support this, assuming I don’t make excessive bad cuts or drilling mistakes.

- Reasoning:
  - When it comes time to cover electronics in video, running **48V and 24V rails simultaneously** is likely too much for most builders.
  - It increases complexity and frustration, and adds significant cost.
  - That setup makes sense for my **test rig**, and I may still document it on the blog and in advanced videos.
  - However, for **how-to and build-guide videos**, a simpler, more approachable configuration is the better teaching choice.

- The **second build** will:
  - Omit the frame stiffeners.
  - Use a more conservative, builder-friendly electronics setup.

- Saner electronics options under consideration for the second build:
  1. **Mellow High-Speed Super 8 Pro (3 + 5 HV)**
  2. **Makerbase SKIPR all-in-one board**
  3. **400W 24V power supply**

- These components will need to be tested for **repeatability and long-term reliability** before being considered for inclusion in any future kits.

## 2025-12-14

- Watching back the YouTube video: brackets printed on the Sovol show visible shift artifacts. Parts are still square, but for example/validation pieces, slow the printer down or use the Vorons. ABS prints benefit from lower speeds for both strength and dimensional precision. Note for future part confirmations and videos.
- Watching video back: it may be useful to record two points of view at once. Record my face and talking while recording my hands working. Easy way to do this, without compromising "I am not a youtuber, I have no intention of spending money on recording equiptment". Use the MacBook to record me, use the iPhone and the $20 arm I bought to record me working. This will be useful in future videos when we're building a large frame, etc. As I can switch views. This adds ~3 minutes of video editing time.

## 2025-12-11

- Reversal of original CAD separation. All CAD now housed in the NF3D-Trident file. This will improve workflow.
- Turned 1 bracket into 12 around the top. Loosely (messy CAD) placed them until I add the T-nuts and the M5 bolts.
- With the shortened printer, this stiffener design will work. If I built it taller, may need to consider weight. How much does 48 M5 bolts and 48 T-nuts add?
- This is the design for this shortened dual gantry Trident. May reconsider the number of braces if we decide to release this printer in kit form. Added stiffness is still more important for this first printer.

## 2025-12-09 — Top Frame Stiffeners Created in CAD, Validated by Printing

- 10mm × 20mm × 60mm corner brackets designed, 2 bolts per rail into T-nuts
- Tried to keep the aesthetics of the printer correct
- Will use these brackets around the top frame, and also at each X/Y corner once non-interference is confirmed
- Shortened build volume further stiffens the frame and benefits dual-gantry 48V motion

**STEP BACK** — separating CAD into parts was a bad idea. All new and future CAD will live in a unified NF3D Dual Gantry CAD directory. Original Trident CAD retained for reference.

## 2025-12-05 — Working CAD Structure / Workflow Started

- Designing frame stiffeners first
- Electronics bay next — flipped with a see-through panel for easy access
- Pi-through skirts housed in Electronics Bay CAD
- Early decisions here affect many downstream designs

## 2025-12-03 — CAD Structure & Workflow Decisions

- Established long-term CAD workflow for NF3D Trident POC
- Created modular structure:
  - ElectronicsBay
  - Frame
  - Gantry
  - Panels
  - NF3DReassembled
  - Trident-Original-Cad

- Reasoning:
  - Avoids a single massive Fusion file
  - Faster subsystem iteration in VR
  - Preserves a clean reference baseline

- Conclusion:
  - CAD workflow is now stable
  - Supports NF3D philosophy: design openly, iterate quickly, build only what’s validated
