## Design notes added 2025-11-25. Gives a place to share thoughts when we edit CHANGELOG.MD and a place to show people why we chose X or Y.

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
- See **DESIGN-NOTES.md → 2025-12-19 – Gantry Design Thoughts**


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
