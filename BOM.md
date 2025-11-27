# **NF3D Trident – Prototype BOM (NF3D Voron Trident Build 0.1)**
### **Updated: Nov 26, 2025**
### *Evolving development bill of materials – premium prototype build*
### *Updated as parts are ordered, will finalize with the first/second working prototypes*

This BOM describes the current hardware for the **NF3D.000001 premium prototype**.  
It is intentionally overbuilt to allow testing, tuning, and development.  
It does **not** represent the final BOM or any possible kit.

---

## 🧠 Host Controller / UI
- Raspberry Pi 4 — 4 GB - selected specifically over the 5 for usb power from Octopus pro (ie no 5v buck to power a pi)
- Elecrow 5″ HDMI Touchscreen (800×480, USB-powered, external via skirt passthrough)

---

## 🔧 Main Motion & Control Electronics
- BIGTREETECH Octopus Pro V1.1 (H723 MCU)  
- 8× TMC5160T Pro stepper drivers  
- RJ11 → CAN cable (Octopus → UTC)

### CAN Toolhead Architecture
- 2× BTT EBB36 CAN V1.2 (G0B1)  
  - Onboard ADXL345 accelerometers  
- 2× BTT UTC V2.1 (Triple CAN Output hubs)

---

## 🎯 Probing & Filament Sensors
- CNC Lab CNC Voron Tap V2/V1  
- 2× SFS V2 Smart Filament Sensors

---

## ⚙️ Motion System — Custom NF3D Motors

### X/Y/Z Axis Motors
- Custom Hanspose NEMA 17 – 42×48 mm – 0.9°  
- 3× Hanspose NEMA 17 – 42×48 mm – 0.9°  
  - Integrated 250 mm T8×2 (1-start) lead screws  
  - Shorter build height selected for early prototypes / stiffest frame behavior

### Extruder Motors
- 2× Hanspose 36 mm Pancake – 0.9°  
  - High-resolution extruder motors

---

## 🛠️ Frame & Linear Motion Components

### Aluminum Extrusions
- **10× 2020 Black Aluminum Extrusions – 1220 mm**  
  - For cutting, drilling, and tapping for NF3D Trident 300 build  
  - First prototype (Frame #1)

### Linear Rails
- **3× MGN9 – 250 mm** (Z-axis rails)  
- **4× MGN9 – 300 mm** (X/Y rails)  
- **2× MGN12 – 300 mm** (X/Y rails, carriage/gantry structure)

---

## 🔌 Power System

### Power Supplies
- **Mean Well LRS-350-48 — 48 V, 7.3 A, 350.4 W**  
  - Selected due to limited Canadian availability of 450 W units

### Buck / Step-Down Conversion
- **DROK CNC DC Buck Converter with Meter**  
  - 6–70 V → adjustable 0–60 V, 10 A / 600 W  
  - Provides regulated 24 V rail from 48 V supply  
  - Integrated volt/amp display for development testing

### Power Distribution
- **12-position Dual-Row Covered Screw Terminal Block — 600 V, 15 A**  
  - Clean separation of 48 V and 24 V rails  
  - Allows modular wiring and future removable power harnesses

### Bed Power Switching
- **Omron G3NB-210B-1 Solid State Relay (SSR)**  
  - Input: 5–24 VDC  
  - Output: 24–220 VAC, 10 A  
  - Used for early testing of high-voltage bed heaters

---

## 💡 Lighting

### Chamber Lighting
- EMITEVER 24 V COB LED Strip – 5000 K, Ra95+, IP30 (16.4 ft)

### Toolhead RGB
- 2× circular RGB LED boards (5-LED each)  
  - Mounted behind clear NF3D logo windows

---

## 📷 Camera System
- Arducam OV5647 – 5 MP CSI camera  
- Extended CSI ribbon cable (for gantry-proximal mounting)

---

## 📝 Still To Select / Order

### Power System
- Optional 5 V buck converter (if Pi is powered from printer PSU)

### Hotend & Heating System
- Hotends (Rapido HF, Dragon HF, Revo HF/RF, etc.)  
- Nozzles (hardened and high-flow)  
- Heater cartridges (24 V or 48 V)  
- Thermistors or PT100/PT1000

### Cooling
- 24 V hotend fans  
- 24 V part-cooling fans  
- 24 V chamber fans  
- Optional:  
  - Bed-cooling fans  
  - Enclosure filtration (carbon / HEPA)

### Bed Heating
- Bed heater pad (voltage TBD)  
- Bed thermistor or thermocouple  
- Bed insulation  

