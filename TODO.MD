# NorthForge3D Trident — TODO

This file tracks short-term engineering and documentation tasks for the Trident dual-gantry proof-of-concept.  
Items here reflect the latest active development and will change frequently.

---

## 🧱 CAD Tasks

- [ ] **Redesign Trident Gantry — Timeframe: Weeks 1–3**
    - **2040 profile version** — significantly increase stiffness for two toolheads moving at ~15,000 mm/s² accelerations.
    - Design in CAD.

- [ ] **Design corner brackets for top and bottom frame interface**
    - Bolt-through 2040/2020 frame reinforcement brackets.
    - Target: significantly increase frame rigidity and torsional stiffness.
    - Integrate mounting bosses for panels and cable routing where possible.

- [ ] **Redesign Trident bearing stacks for dual-gantry support**
    - New bearing stack system for **2040 crossmembers**.
    - Two XY motors above / two XY motors below configuration.
    - Bearing stack assemblies will **bolt through the frame** to stiffen the entire gantry structure.
    - Ensure compatibility with dual independent toolhead carriages.

- [ ] **Begin layout for the NF3D custom bottom section — Week 3-4**
    - Begin once both gantry variants are complete.
    - Focus areas:
        - Inverted electronics concept
        - Cable routing channels
        - Serviceability and access
        - Mounting structure for power and logic hardware

---

## 📄 Documentation Tasks

- [ ] Add current gantry render to `/docs/images`
- [ ] Write a short overview of the Trident’s purpose in `/docs`
    - Emphasize its role as the motion-system R&D platform for the Deuce.
    - Clarify that this is a proof-of-concept, not a production machine.

---

## 🧪 Testing Tasks

- [ ] **Order frame kits and bearing sets**
    - Immediately after both gantry variants are designed.
    - Include additional extrusions to allow quick iteration during testing.

- [ ] **Print gantry component STLs for validation**
    - Begin printing immediately after completing both gantry designs.

- [ ] **Build gantry outside the printer**
    - Validate:
        - Motion smoothness
        - Belt routing and clearances
        - Bearing alignment
        - Structural rigidity
        - Dual-gantry choreography potential
    - Begin once extrusions arrive.  ( not ordered yet)

---

This file will be updated as development progresses.
