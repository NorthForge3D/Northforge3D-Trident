# NorthForge3D Trident – Proof-of-Concept Platform  
### A development platform for the upcoming **NorthForge3D Deuce** – a true dual-gantry IDEX 3D printer.

---

## ⚠️ **Experimental Project – Do Not Build Yet**

This repository is under **active development** and contains **early, unstable, and rapidly changing work**.

If you'd like to follow the progress of this proof-of-concept—and receive updates on our full production printer—you can subscribe here:

👉 **Follow the Trident Build and the Deuce as They Evolve**  
https://northforge3d.com/forge-with-us/

Also visit our main site as the Deuce evolves:  
https://northforge3d.com

When this design stabilizes, we will publish a **full video series** documenting every stage of building a NorthForge3D Trident.

---

# ⚡ What This Project Is

This repository documents the **engineering, testing, and evolution** of the NorthForge3D **Trident-based dual-gantry test platform**.

It is **not** the Deuce, and it is **not** intended as a drop-in Voron derivative.

Instead, this machine serves as the **R&D sandbox** for developing:

- Dual-gantry motion  
- Toolhead choreography  
- Collision-avoidance logic  
- Motion refinement  
- Lightweight toolheads  
- Klipper tuning  
- 0.9° high-resolution motors  
- Pancake stepper extrusion  
- Early electronics layout for the Deuce  
- General mechanical innovations

Everything here is **iterating weekly**. Expect redesigns, experiments, and occasional chaos.

---

# 🔧 Goals of the Proof-of-Concept Printer

## ✔ Validate Dual-Gantry Motion  
We need a reliable platform to test:

- Independent toolheads  
- Parallel/mirror print modes  
- Mixed toolpaths  
- Coordinated high-speed motion

## ✔ Redesign Major Subsystems  
While Trident-footprint inspired, this machine will diverge significantly:

- Complete redesign of the **bottom section**  
  - No Voron skirt  
  - **Inverted electronics** visible inside the chamber  
  - Clean, service-friendly layout
- Raspberry Pi on a custom plate with **side-facing ports**  
- A redesigned **dual (eventual quad) gantry**  
- Lightweight toolheads  
- Filament cutter – v2  
- New cable routing systems  
- Modified or fully custom gantry components  
- Custom motors, pulley arrangements, and belt routing as needed

## ✔ Prototype a Production-Forward Layout  
This POC is used to test:

- Thermal management  
- Cable access and serviceability  
- Component placement  
- Mechanical accessibility  
- Toolhead maintenance paths  
- The aesthetic and functional “feel” of a future NorthForge3D printer

---

# 🔩 Hardware Decisions (So Far)

- **0.9° NEMA 17 Motors** – 0.54 Nm, 42×48 mm  
- **0.9° Pancake Steppers** for toolheads  
- **T8×2 (single start) Lead Screws** for ultra-fine Z resolution  
- **Klipper-based electronics**  
- Raspberry Pi with external-facing I/O  
- Additional hardware evolving as testing continues

---

# 🚧 Status: Early Development

This repository is currently being **cleaned**, **reorganized**, and **realigned** to the new design direction.

Over the next phase:

- Voron-specific content will be fully removed  
- Bottom section redesign will be introduced  
- Early gantry tests will be published (coming weeks)  
- CAD development will begin in Fusion 360  
- Week #1 development log will be added

After that: expect **frequent changelogs** as the machine takes shape.

---

# 📅 Development Logs

Logs will be posted regularly as meaningful progress occurs, covering:

- CAD progress  
- Mechanical R&D  
- Firmware advances  
- Toolhead experiments  
- Photo/renders as the project evolves  
- Iterative design changes  
- Lessons learned and upcoming plans  

Our goal is to **document the birth of a printer in real-time**.

---

# 🧪 This Is **Not** the Deuce

The final **NorthForge3D Deuce** will be:

- Much larger  
- Fully enclosed  
- Built on a custom extrusion frame  
- Featuring production-grade electronics  
- Running refined dual-gantry mechanisms  
- Built with collision-resistant logic  
- Outfitted with custom motors, pulleys, and mechanical systems  
- Designed with full internal lighting and service access paths

This proof-of-concept exists solely to **perfect motion, firmware, and mechanical fundamentals** before the production machine.

---

# 🔗 Follow the Project

👉 **Website**  
https://northforge3d.com

👉 **Subscribe for Development Updates**  
https://northforge3d.com/forge-with-us/

👉 **Deuce Engineering Blog**  
https://northforge3d.com/forge-updates/deuce-updates/

👉 **Facebook (Daily Updates)**  
https://www.facebook.com/NorthForge3D/

👉 **YouTube** (Full build series coming)  
https://www.youtube.com/@northforge3d

👉 **Instagram**  
https://www.instagram.com/northforge3d/

---

# 📜 License

This project is currently released under the **GNU GPLv3** license.

Once the proof-of-concept stabilizes into a working dual-gantry printer, we will clearly identify:

- Which components originate from Voron Trident  
- Which components are original NorthForge3D designs  

The license will remain the same.

---

# 🤝 Contributions

This is an active engineering development project.  
Contributions and discussion are welcome—just understand things move fast and may be reworked often.

Open an issue or PR if you’d like to collaborate.

---

# 🛠 Changelog

**Nov 19, 2025**  
- Removed Trident-specific STLs, drawings, and manuals  
- Transitioned to CAD-only workflow  
- Preparing custom modifications for dual-gantry testing  
- STLs will be added only after printed and validated  
- Expect next major update in ~2–3 weeks (around the time custom 0.9° motors arrive)
