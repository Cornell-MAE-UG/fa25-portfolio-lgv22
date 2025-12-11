---
layout: project
title: Fluid Mechanical Dissection
description: Disassembly and fluid-mechanics analysis of a hydrostatic transaxle.
technologies: [Autodesk Fusion, Fluid Mechanics]
image: assets/images/fluids1.jpg
---

For this project, we were asked to take apart a machine and explain how it works using concepts from fluid mechanics. My group dissected a hydrostatic transaxle from a lawn tractor. My role was opening the unit, documenting the internal components, and taking the measurements needed for the flow and displacement calculations.

###### What we analyzed
Inside the transaxle is a hydrostatic pump–motor loop. When the input shaft rotates, the pump uses a tilted swash plate to drive pistons and push fluid through a closed loop. The motor section receives that flow and converts it back into rotation to drive the wheels.  
We identified the pump pistons, motor pistons, swash plate, case ports, and drive shafts as we disassembled the unit. 

![ANSYS image]({{ "/assets/images/fluids2.png" | relative_url }}){: .block-image}

![ANSYS image]({{ "/assets/images/fluids3.png" | relative_url }}){: .block-image}

![ANSYS image]({{ "/assets/images/fluids4.png" | relative_url }}){: .block-image}

###### Core fluid-mechanics concepts
We explained the device using:
- Positive-displacement pump flow: $$Q_p = D_p(\theta)\,\omega_p$$
- Swash-plate geometry: $$D_p(\theta) = D_{\max}\sin\theta$$
- Motor speed relation from continuity 
- Torque generation from pressure on each piston 
- Hydraulic power and efficiency  
- Leakage modeling using laminar thin-film flow  

These equations came directly from our measurements of piston diameter, stroke length, and swash-plate angle. 

###### Quantitative results
Using our measured displacement values:
- For a 7 GPM flow rate, the motor speed was about 2200 rpm for the small-displacement case and 1100 rpm for the larger one.  
- These correspond to vehicle speeds of ~8 mph and ~4 mph. 

###### My contributions
- Disassembled the transaxle and identified components  
- Took all dimensional measurements for displacement and flow calculations  
- Helped work through the governing equations and performance estimates  
- Co-wrote and filmed the final explanation video

###### Final video
**Fluid mechanical dissection video**  
[Watch on YouTube](https://www.youtube.com/watch?v=19PIwncbsFY)
