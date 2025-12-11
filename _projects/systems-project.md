---
layout: project
title: Autonomous Sailboat Control
description: State-space model and PD controller for a line-following sailboat.
technologies: [MATLAB, ODE Modeling, Control Systems]
image: /assets/images/sailboat1.png
---

For this project, our group modeled an autonomous sailboat that can follow a desired heading while rejecting wind disturbances. My role was defining the state-space model, the angle-disturbance formulation, and the ODEs that the controller and simulation rely on.

## Model Setup
We simplified the full 3-DOF sailboat dynamics down to the states that matter for line following:  
- heading error ϕ  
- yaw rate ω  

I derived the equations for:
- kinematics (θ̇ = ω)  
- yaw dynamics with rudder torque, damping, and wind torque  
- linearization to get constants \(k_d\), \(k_r\), and \(k_w\)  
- the final state-space form  

The final system is:

\[
\dot{x} =
\begin{bmatrix}
0 & 1 \\
0 & -k_d
\end{bmatrix}x
+
\begin{bmatrix}
0 & 0 \\
k_r & k_w
\end{bmatrix}
\begin{bmatrix}
\delta_r \\
w_d
\end{bmatrix}
\]

with output \(y = [1\ \ 0]x\).  
This reduced model is what the controller and simulation run on.

![ANSYS image]({{ "/assets/images/sailboat2.png" | relative_url }}){: .block-image}

![ANSYS image]({{ "/assets/images/sailboat3.png" | relative_url }}){: .block-image}

## PD Controller
Using the linear model, we built a PD controller for the rudder:

\[
\delta_r = K_p(\theta_{\text{ref}} - \theta) - K_d \omega
\]

The characteristic equation from the closed-loop A-matrix gave us the formulas for \(K_p\) and \(K_d\). These match the table in the report. 

## MATLAB Simulation
The controller and state-space ODE were coded into MATLAB. The simulation solves for θ(t) and ω(t), and compares the boat’s heading with the reference.  
The results show the controller pulling the sailboat to the desired angle from any initial orientation. 

## MATLAB Animation
Our model also drives a full animation of the boat. The animation updates:  
- the hull and sail orientation using rotation matrices  
- forward motion at a constant speed  
- heading displayed live on the figure  

The animation loop uses the θ(t) output from my ODE model. 

## My Contributions
- Defined the state variables, disturbance**, and input structure  
- Built the *tate-space model used in all downstream work  
- Derived the linearization and constants for damping, rudder effectiveness, and wind torque  

## Summary
The project produced a simplified but functional control-oriented sailboat model, a PD controller, a simulation that tracks heading, and a full MATLAB animation. My contribution established the mathematical foundation the rest of the work depends on.

Back to Projects
