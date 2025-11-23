# NorthForge3D Trident — Changelog  
All development updates for the Trident dual-gantry proof-of-concept platform.  
This log documents progress as the machine evolves toward the NorthForge3D **Deuce**.

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
