---
## NF3D Trident – Prototype BOM (NF3D Voron Trident Build 0.1)
### Evolving development bill of materials – premium prototype build

This BOM describes the current hardware for the **NF3D.000001 premium prototype**.  
It is intentionally overbuilt to allow testing, tuning, and development.  
It does **not** represent the final BOM or any possible kit.

---

## 🧠 Host Controller / UI
- Raspberry Pi 4 — 4 GB
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
- Custom Hanspose NEMA 17 – 42×48mm – 0.9°
- 3× Hanspose NEMA 17 – 42×48mm – 0.9°  
  - Integrated 250 mm T8×2 (1-start) lead screws

### Extruder Motors
- 2× Hanspose 36 mm Pancake – 0.9°  
  - High-resolution extruder motors

---

## 💡 Lighting

### Chamber Lighting
- EMITEVER 24V COB LED Strip – 5000K, Ra95+, IP30 (16.4 ft)

### Toolhead RGB
- 2× circular RGB LED boards (5-LED each)  
  - Mounted behind clear NF3D logo windows

---

## 📷 Camera System
- Arducam OV5647 – 5 MP CSI camera (CSI interface)
- Extended CSI ribbon cable (for gantry-proximal mounting)

---

## 📝 Still To Select / Order

### Power System
- 48 V PSU
- 24 V PSU **or** 48→24 V DC-DC converter
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
- SSR or MOSFET (appropriate to heater voltage)
- Bed thermistor or thermocouple
- Bed insulation
