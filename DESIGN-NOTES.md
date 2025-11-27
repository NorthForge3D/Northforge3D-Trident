## Design notes added 2025-11-25. Gives a place to share thoughts when we edit CHANGELOG.MD and a place to show people why we chose X or Y. 


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
