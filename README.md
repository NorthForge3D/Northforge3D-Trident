# NorthForge3D Trident – Proof-of-Concept Platform  
### A development platform for the upcoming **NorthForge3D Deuce** – a true dual-gantry IDEX 3D printer.

---

> ⚠️ **Experimental Project – Don’t Build Yet**
If you'd like to subscribe to updates as this printer, and our full production printer, you can do so here: 👉 **Follow The Trident Build and the Deuce as it Evolves.** https://northforge3d.com/forge-with-us/. Also be sure to check out our upcoming production machine (as it too evolves) at https://northforge3d.com

When we are finish with this design you can expect a full video series documenting every step of building a Northforge Trident. > ⚠️

## ⚡ What This Project Is  
This repository documents the **design, testing, and evolution** of the NorthForge3D Trident-based proof-of-concept printer.  
It is **not** the final Deuce, and it is **not** intended to be a drop-in Voron derivative.

Instead, this machine serves as the **engineering sandbox** for testing:

- Dual-gantry motion coordination  
- Toolhead choreography  
- Collision-avoidance logic  
- Motion refinement  
- Lightweight toolhead design  
- Firmware tuning (Klipper)  
- High-resolution motors (0.9° steppers)  
- Extrusion tests with pancake steppers  
- Early versions of the Deuce electronics layout  
- General mechanical R&D

Everything here is evolving rapidly.  
Expect weekly changes, redesigns, and experiments.

---

## 🔧 Goals of the Proof-of-Concept Printer

### ✔ Test dual-gantry motion principles  
Before developing the full Deuce machine, we need a reliable testbed for:
- Independent gantries  
- Parallel/mirror modes  
- Mixed toolpaths  
- High-speed synchronized printing

### ✔ Redesign major components  
Even though this starts from a Trident footprint, and it still is a trident at it's core, we plan to change:
- Complete redesign of the **bottom section**  
  - No Voron skirt  
  - **Inverted electronics**  
  - Visible, service-friendly layout from inside the chamber  
- Custom plate to mount a Raspberry Pi with **side-facing USB/HDMI/network ports**, similar to a production machine  
- Redesigned dual gantry (eventual 4 gantry) for two independent motion systems
- Custom lightweight toolheads  
- Integrated filament cutter (second iteration)
- New cable management system  
- Modified or fully custom gantry components  
- Custom motors, possibly belts, and pulley arrangement where needed

### ✔ Develop a clean, production-forward internal layout  
This proof-of-concept printer will be used to test:
- Thermal routing  
- Cable access  
- Component placement  
- Build accessibility  
- Toolhead maintainability  
- The overall “look and feel” expected of a future NorthForge3D product

---

## 🔩 Hardware Decisions (So Far)

- **0.9° Stepper Motors** for precision motion  
  - 0.54 Nm holding torque (42×48 mm)
- **0.9° Pancake Steppers** for compact extruder motion
- **T8×2 (single start) Lead Screws** for fine Z-resolution control
- Klipper-based electronics  
- Raspberry Pi with external-facing ports  
- All hardware and layout subject to change as testing evolves

---

## 🚧 Status: Early Development  
This repository is **actively being cleaned and restructured**.  
Over the next few days:

- Voron-specific parts will be removed  
- The bottom section will be replaced with a clean NorthForge3D design  
- Early gantry redesigns will be posted (coming in a few weeks)
- Initial CAD work will begin in Fusion 360  
- A Week #1 development log will be added

After that, expect frequent changelogs as the machine evolves.

---

## 📅 Weekly Development Logs  
A new update will be posted at least once per week, covering:

- CAD changes  
- Mechanical redesigns  
- Motion experiments  
- Firmware tuning  
- Toolhead prototypes  
- Mistakes, fixes, and improvements  
- Future plans  
- Photos, renders, or video clips  

The goal is to **let the world watch us build a 3D printer from the ground up**.

---

## 🧪 This is NOT the Deuce  
The final Deuce will:

- Feature a **much larger** build volume  
- Use a custom extrusion frame  
- Have a full enclosure  
- Feature a production-grade electronics layout  
- Use refined, purpose-built gantries  
- Include collision-resistant logic in firmware  
- Feature advanced toolhead coordination  
- Use custom motors and mechanical components  
- Have internal lighting, cable routing, and service paths optimized for production use

This proof-of-concept simply provides a **test environment** to perfect motion systems, firmware behaviors, and mechanical fundamentals first.

---

## 🔗 Follow the Project  
We are documenting this journey publicly across multiple platforms:


👉 **Website**  
https://northforge3d.com

👉 **Follow The Trident Build and the Deuce as it Evloves.**  
https://northforge3d.com/forge-with-us/

👉 **Deuce Engineering Blog**  
https://northforge3d.com/forge-updates/deuce-updates/

👉 **Facebook Page (Daily Updates)**  
https://www.facebook.com/NorthForge3D/

👉 **YouTube Channel (Coming Soon)**  
Channel Here https://www.youtube.com/@northforge3d  Subscribe for updates, no content until the actual build starts. Full step by step build series to be added. 

👉 **Instagram **  
Short clips, photos, and behind-the-scenes development.
https://www.instagram.com/northforge3d/
---

## 📜 License  
This proof-of-concept repository is released under a GNU V3 License: once the fundamental design stabilizes and it is a working Dual Gantry printer we will clarify what is Trident and what is Northforge3d. The license will remain the same. 

---

## 🤝 Contributions  
This is an active engineering project, not a finished printer.  
Outside contributions are welcome, but the design is evolving rapidly.  
Open issues or PRs if you want to discuss ideas, improvements, or testing.

---

## 🛠 Changelogs  
Changelogs will appear here as development progresses.

Nov 19th 2025. Removed Trident-Specific stls, drawings, manual etc. Working purely with CAD at this point to customize the trident for our needs, look, and feel. STLs will begin to appear as we are printing them and working towards a fully functional dual-gantry Trident. CAD will be the slowest part, expect the next change log in 2-3 weeks (about the same time our custom 0.9 Nema 17 motors arrive).


