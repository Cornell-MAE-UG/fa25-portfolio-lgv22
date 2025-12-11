---
layout: project
title: Torque Wrench
description: Custom torque wrench designed using hand calcs, CAD, and FEM.
technologies: [Fusion, ANSYS, MATLAB]
image: /assets/images/ansys2_2.png
---

This project was the final design assignment for MAE 3270. The goal was to design a non-ratcheting 3/8" drive torque wrench rated for 600 in-lb, and hit specific requirements for strength, fatigue, fracture, and strain-gauge sensitivity. Hand calculations, CAD, and FEM were all required.  

---

###### Baseline → My Design
We were given a baseline M42 steel wrench to analyze first. It met strength and fatigue requirements but failed the sensitivity requirement (0.38 mV/V vs the required 1.0 mV/V).  
This created the main design goal: increase strain at the gauge while still meeting all safety factors.  
![ANSYS image]({{ "/assets/images/ansys1_1.png" | relative_url }}){: .block-image}

![ANSYS image]({{ "/assets/images/ansys1_2.png" | relative_url }}){: .block-image}

![ANSYS image]({{ "/assets/images/ansys1_3.png" | relative_url }}){: .block-image}

I wrote MATLAB code to automate the hand-calc process so I could iterate dimensions, material properties, and gauge location which is attached at the bottom of this page.

###### Material
I selected Ti-6Al-4V because:
- high strength-to-weight ratio  
- good fatigue behavior  
- lower stiffness than steel means higher strain, which helps sensitivity  


###### CAD Model
I built the final geometry in Fusion based on the MATLAB-optimized dimensions. 
![ANSYS image]({{ "/assets/images/ansys2_1.png" | relative_url }}){: .block-image}

###### FEM Setup
In ANSYS:
- fixed support applied to the upper 0.4 in of the drive  
- downward load equal to 600 in-lb / 16 in = 37.5 lb applied at the handle  
- mesh refinement focused around the fillet and gauge region  


###### FEM Results
- Max normal stress: ~48–52 ksi  
- Tip deflection: 0.382 in  
- Strain at gauge: ~413 µε  
- Principal stress field shows the expected peak around the drive fillet  
- Normal strain contour shows smooth bending distribution across the handle  

![ANSYS image]({{ "/assets/images/ansys2_2.png" | relative_url }}){: .block-image}

![ANSYS image]({{ "/assets/images/ansys2_3.png" | relative_url }}){: .block-image}

![ANSYS image]({{ "/assets/images/ansys2_4.png" | relative_url }}){: .block-image}

These results satisfy the required strength, fracture, and fatigue safety factors.  


###### Sensitivity
Using the FEM strain at the gauge location:

sensitivity = 0.413

This meets the 1.0 mV/V requirement using a full bridge configuration, and is within range of what the project description states is acceptable.  


###### Strain Gauge Selection
I selected a double-linear bending gauge (0.354" × 0.354"). It fits cleanly on the gauge surface and aligns with the dominant bending strain.  


###### Summary
- Automated hand-calcs in MATLAB  
- CAD geometry guided by analytical results  
- FEM validation in ANSYS  
- Design meets all safety factors and sensitivity targets  
- Material and geometry choices directly tied to project constraints

This project pulled together everything from the course: materials, fracture, fatigue, strain gauging, and FEM.  

