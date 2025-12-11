---
layout: project
title: OpenUp – Easy-to-Clean Water Bottle
description: Horizontally split, clamp-sealed bottle that makes deep cleaning actually doable.
technologies: [Autodesk Fusion, 3D Printing, O-Rings, Prototyping, DFM/DFS/DFQ]
image: assets/images/waterbottle4.png
---

Most reusable bottles are great at keeping water cold and terrible to clean. Tiny necks, deep bottoms, and complicated lids trap grime and smell. OpenUp is our attempt to fix that: a horizontally split water bottle that opens in the middle so you can actually reach every surface, clean it, and put it back together leak-free.

### Problem & User Research

We started with the question:  
> “If you own a reusable bottle, how often do you actually clean it—and what makes it annoying?”

Through interviews with students and working adults, we heard the same themes:
- Bottles are cleaned far less often than people think they should.
- People resort to shaking soapy water inside because they can’t reach the bottom.
- Sippy tops, small necks, and deep crevices feel “impossible” to clean.
- Several people admitted they eventually abandon or replace bottles when they start to smell.

From this we framed our project goal:

> **Design a reusable bottle that’s easy to clean thoroughly, without special tools, and still works in everyday life (cupholders, backpacks, etc.).**

### Design Concept – Split Bottle + Clamp Seal

Our final concept, OpenUp, is a bottle made from two halves that split horizontally at the midpoint:

- A small upper neck for comfortable drinking.
- A wider body so a user can get their hand and a cloth inside.
- The halves join at the midline using low-profile steel draw latches so the exterior stays smooth enough for cupholders and backpack pockets.
- A rubber O-ring in a machined groove provides the seal between the halves.
- The cap uses its own O-ring so the bottle is leak-free when reassembled.

In CAD, we modeled:
- The two shell halves with mating geometry at the split.
- Flat pads for the clamps so they sit flush and don’t catch on bags.
- A controlled O-ring groove sized for the compression we needed.

![CAD pic of waterbottle]({{ "/assets/images/waterbottle1.png" | relative_url }}){: .inline-image-l}
![CAD pic of waterbottle 2]({{ "/assets/images/waterbottle3.png" | relative_url }}){: .inline-image-l}

### Prototyping & Fabrication

For our first functional prototypes, we:
- 3D printed the top and bottom halves in plastic to check fit, ergonomics, and clearances.
- Bought the hardware and sealing elements:
  - Steel draw latches
  - Multiple candidate O-rings (different profiles and diameters)
  - Off-the-shelf cap

We used adhesive (resin/epoxy) to attach the clamps for iteration and later used heat-set inserts and bolts as a more robust solution.

### Testing

We built a test plan around three questions:  

1. **Can you really clean it better?**  
   - With the bottle split, we tried reaching every corner surface with a washcloth.  
   - The top half was easily reachable; the bottom half was almost reachable, but we identified that the diameter needed to be slightly larger so a normal hand could comfortably scrub the bottom.  

2. **Does it seal?**  
   - We closed the clamps, filled the bottle with water, and watched for leaks at the midline.  
   - A misalignment in clamp heights caused uneven O-ring compression, which led to leaks on one side of the joint.  
   - We also found that a misprinted cap (sanded too aggressively) exposed internal print pores, letting water bypass the cap O-ring and leak even though the sealing concept itself was robust.

3. **Can it survive normal abuse?**  
   - We performed a drop test from table height.  
   - The 3D-printed body survived with only cosmetic scuffs.  
   - The resin-bonded clamp partially failed: it stayed on through the drop but snapped off when unclamped afterwards, showing that the adhesive method wasn’t reliable enough.

From these tests we concluded:
- The overall concept works (split bottle + clamps + O-ring).
- Clamp attachment and alignment are critical.
- We needed minor geometry tweaks for comfort and cleanability (larger diameter, softer edges).

### Design for Manufacturing, Sustainability & Quality

As the concept matured, we re-imagined the final production version:

##### Design for Manufacturing (DfM)
- Move from thick 3D-printed walls to thin, hollow stainless-steel shells.
- Use processes appropriate for 100+ unit production, such as deep drawing or metal forming for the body and spot-welding for clamps.
- Integrate clamp mounting bosses directly into the CAD so clamp locations are fixed and symmetric.

##### Design for Sustainability (DfS)
- Replace the short-life plastic prototype with a **dual-layer stainless-steel body**:
  - Longer lifespan → fewer replacements → less waste.
  - Air gap between layers doubles as **thermal insulation**.
- Reduce wall thickness to cut material usage and carbon footprint while keeping durability.
- Use a bill of materials that relies on standard, replaceable O-rings and hardware.

##### Design for Quality (DfQ)
- Add larger fillets and rounded edges at all openings to make it comfortable to reach in and clean.
- Add an optional grippy rubber coating to improve ergonomics and perceived quality.
- Replace adhesive-bonded clamps with spot-welded or mechanically fastened clamps for long-term reliability.

### Outcome & Next Steps

Our final recommendation is that OpenUp should move forward with the current core architecture:

- The horizontal split + clamp + O-ring system solves the biggest pain point: actually being able to clean every surface.
- Usability tests confirmed that the bottle still behaves like a “normal” bottle: it fits into pockets, feels good in the hand, and isn’t too heavy.
- The remaining work is refinement, not a fundamental redesign:
  - Dial in clamp geometry and attachment for production.
  - Finalize stainless-steel wall thickness and insulation strategy.
  - Iterate on diameter and ergonomics so every user can comfortably scrub both halves.

OpenUp takes a problem most people quietly ignore—gross, hard-to-clean bottles—and makes the solution mechanical.
