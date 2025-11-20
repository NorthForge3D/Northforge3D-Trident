# Firmware – NorthForge3D Trident Proof-of-Concept  
This folder contains firmware, macros, and Klipper-related files used to develop and validate the Trident-based dual-gantry platform.

The firmware here exists to support **experimentation**, not stable releases.

---

## 🎛 Firmware Stack  
- **Firmware:** Klipper  
- **Host:** Linux SBC (Raspberry Pi or equivalent)  
- **MCU:** High-current 3D-printer controller (final board selection coming soon)  

The goal of this firmware folder is to support:

- Dual-gantry motion testing  
- Collision-avoidance experiments  
- Parallel and mirror printing modes  
- Tuning for 0.9° steppers and fine-pitch lead screws  
- Toolhead choreography and motion safety

---

## ⚠️ Not Drop-In Configuration  
Anything here should be treated as **unsafe for general use** unless you fully understand:

- Stepper currents  
- Pin mappings  
- Kinematics  
- Heater safety  
- Motion limits  

This firmware is tied directly to our prototype hardware and may change daily.

---

## 🔧 Planned Structure  
As things stabilize, this folder will likely include:

- `klipper/printer-nf3d-trident.cfg` – main machine profile  
- `macros/` – dual-gantry tools, parking routines, collision logic  
- `extras/` – helper config files and tuning profiles  

---

## 📡 Follow the Firmware Development  
If you're interested in how this evolves — and eventually, in the **full build-along firmware series** — you can follow the project here:

👉 **Subscribe for build updates**  
https://northforge3d.com/forge-with-us/

👉 **YouTube** – full Trident build + firmware walkthrough coming soon  
https://www.youtube.com/@northforge3d

👉 **NorthForge3D website**  
https://northforge3d.com

These links are optional, but they give insight into the engineering decisions behind this firmware work.

---

## 🛑 Safety Disclaimer  
This firmware is experimental and should **not** be used on production printers.  
Always validate all limits, currents, and safety systems manually before enabling heaters or motion.
