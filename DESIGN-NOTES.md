## Design notes added 2025-11-25. Gives a place to share thoughts when we edit CHANGELOG.MD and a place to show people why we chose X or Y. 

## 2025-12-11 
    - Reversal of original CAD separation. All CAD now housed in the NF3D-Trident file. This will improved work flow. 
    - Turned 1 bracket into 12 around the top. Loosely (messy cad) placed them until I add the t-nuts, and the m5 bolts. 
    - With the shortened printer, this stiffener design will work. If I built it taller, may need to consider weight. How much does 48 M5 bolts and 48 t-nuts add in weight?
    - This is the design for this shortened dual grantry trident, may reconsider the number of braces if we decide to release this printer in kit form. If I stiffen significantly (I have) but add a 0.5 - 0.8kg of weight at the top, I may reduce movement at the joints but increase the wobble in the aluminum itself. Will try to calculate based on X height vs, X weight at the top frame. Added stiffness is still more important for this first printer. Build volume is shorter, movement at the top is already reduced. Stiffening it will reduce it further over the length of upright we will be using. 

## 2025-12-09 Top Frame Stiffeners Created in Cad, Validated by Printing
    - 10mm x 20mm x 60mm corner brackets designed yesterday, 2 bolts per rail into t nuts
    - Tried to keep the asthetics of the printer correct
    - Will use these brackets around the top frame, and also once confirmed non-interference, at each corner of the X/Y around the top
    - We have decided to build with a volume of 300x 300y 200z ... shortening this printer will further stiffen the frame. 48V rail moving two print heads as quickly as we can without smashing into each other (hopefully) will require every bit of stiffness we can create at the top of the printer where the gantry sits. 

    = STEP BACK - after working with the CAD for a couple of days, separating it out into parts was a bad idea. Will move our new parts, and all future CAD into a NF3D Dual Gantry CAD directory, will keep the original trident file for reference as we work. 

## 2025-12-05 - Working CAD Structure / Workflow Started
    - Desiging the frame stiffeners first
    - Electronics bay next - flipped with a see through panel for easy access
    - PI-Through skirts design will be housed in the Electronics Bay CAD
    - These files may affect other design portions / decisions so it is the place to start

## 2025-12-03 — CAD Structure & Workflow Decisions
    - Tonight’s work established the long-term CAD workflow for the NF3D Trident POC.
    - Created a clean modular layout in `/cad/`:
        - ElectronicsBay
        - Frame
        - Gantry
        - Panels
        - NF3DReassembled (full printer assembly)
        - Trident-Original-Cad (reference only)

    - Reasoning:
        - Avoids working inside a single massive 200-piece Fusion file.
        - Working at the subsystem level is significantly faster in Fusion and VR.
        - Each subsystem can be iterated on without disrupting unrelated geometry.
        - The ‘Reassembled’ directory becomes the single source of truth for alignment and clearance checks.
        - The original Trident CAD must remain untouched so we always have a baseline for comparison.

    - Versioning Thoughts:
        - V0 *is* the printer unless the gantry design fails or a structural issue appears.
        - No need for V1/V2 CAD copies—Git + subsystem separation already gives us rollback safety.
        - Keeping the Trident POC clean avoids carrying unnecessary complexity into the next printer.

    - Why This Matters:
        - A modular CAD structure allows extremely rapid iteration.
        - Lets us test frame stiffeners, electronics bay concepts, panel redesigns, and gantry adjustments without clutter.
        - Provides clarity for contributors or future documentation.
        - Lays the foundation for a consistent CAD workflow across all future NorthForge3D printers.

    - Conclusion:
        - The CAD directory is finally stable.
        - We now have a structure that supports the NF3D philosophy: design openly, iterate quickly, and build only what has been validated.


## 2025-11-26 - Size Desicions - Parts Decision - Experimatal Build
    - Decided on 250mm x 250mm x 200 build volume for first build
        - If we supply these printers as kits - 300 x 300 x 250 (or 300)is more appropriate
        - Smaller build volume for this printer allows for easier frame stiffening (it's shorter) and easier tests of high speeds of dual gantry 48v rail. 
        
## 2025-11-24 - Gantry Starting Point
    - Decided to use zruncho3d dualing gantry as a starting point. See: https://github.com/zruncho3d/DuelingX
    - Verififed on a smaller printer, cad available for 1515, 2020, and 3030. Not verified on sizes above 1515. Probably requires work
    - Starting point for dual gantry collision avoidance klipper using his Dueling Zero. See: https://github.com/zruncho3d/DuelingZero

        Pros - Designed, verified by a few people
             - Working motion system that fits this style of printer
        Cons - Collision avoidance loses some room on the X/Y
             - If we still want 2040 to replace the frame at the gantry we'll have to either:
                - Redsigned it to fit 2040 extrusions
                - Add an additional layer of 2020 inside the the 2040 (a granty rail system bolted inside of a gantry system)
                    - loses 20mm on the X/Y
                    - gains further stiffness at the mid-central top point of the frame. 
                    - stiffen bottom of frame at the corners, stiffen gantry twice, no further cad needed at the top of the printer. 
    - Both options may lead to stretching the frame on the X/Y x 40 mm or so to regain space lost due to dual motion system chose / gantry design chosen to compensate


    ** This will work, it is the start. Exanding a frame only changes frame geometry all designed parts will still work

    ** Need to add a CREDITS.md - Voron, zruncho 

## 2025-11-24 — Z Motor Corner Stiffeners
    - Trident uses Z motors at the front corners of the build. 
         - Easiest way to stiffen front corners is to encase the top 20mm of the motors. Wrap around them, add bolt-through stiffeners to each side of the 2020 at the corners. This adds stiffness.
             - Leads to question - will heat become a concern? 
                - We're running 0.9 steppers with high end high end 5160T Pro drivers
                - Running at 48V
                - Printed parts (for our experimenatl build) from Fiberon ASA-CF (Heat Deflection Temperature (HDT): \(103^{\circ }C\) (@ \(0.45\) MPa)) 
                - Even with fast 10-15mm bed leveling. Should be more than fine, encase away. 
            - This is a high-end build. A kit, or a modder may not make these choices. 
                - Running 24V with 2209s.. Estimated upper temp of motors probably 50 (max 70ish) degrees at high current
                    - Printed parts form ABS or better... should be fine
        - Conclusion
            - Recommend corner braces printed from ABS or better
            - Limit current in Klipper files
