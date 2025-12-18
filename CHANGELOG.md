## Design notes added 2025-11-25. Gives a place to share thoughts when we edit CHANGELOG.MD and a place to show people why we chose X or Y.

## 2025-12-17 – CAD Design & Build Decisions

- For the electronics bay, it will be simpler and cleaner to work from a **separate CAD file**.  
  - This file will include the **full frame** and all **relevant structural reference parts**.  
  - It will be expanded to the **standard build volume of 300 × 300 × 250**.

- This approach allows:
  - A **single source of truth** for skirts, electronics bay, gantry, and panels.
  - All parts to be designed together so **everything fits correctly by default**.
  - Accurate, repeatable dimensions that can be provided directly to suppliers if we decide to offer this printer as a **build kit** (e.g. *cut to this length, drill here*).

- The gantry CAD will be designed **with motion constraints**, allowing motion to be tested in CAD before committing parts to a physical printer.

- I may build this printer **twice**, in parallel, specifically for video documentation.  
  - I already have enough extrusion to support this, assuming I don’t make excessive bad cuts or drilling mistakes.

- Reasoning:
  - When it comes time to cover electronics in video, running **48V and 24V rails simultaneously** is likely too much for most builders.
  - It increases complexity and frustration, and adds significant cost.
  - That setup makes sense for my **test rig**, and I may still document it on the blog and in advanced videos.
  - However, for **how-to and build-guide videos**, a simpler, more approachable configuration is the better teaching choice.

- The **second build** will:
  - Omit the frame stiffeners.
  - Use a more conservative, builder-friendly electronics setup.

- Saner electronics options under consideration for the second build:
  1. **Mellow High-Speed Super 8 Pro (3 + 5 HV)**
  2. **Makerbase SKIPR all-in-one board**
  3. **400W 24V power supply**

- These components will need to be tested for **repeatability and long-term reliability** before being considered for inclusion in any future kits.

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
