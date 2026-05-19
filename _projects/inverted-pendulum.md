---
layout: project
title: "Inverted Pendulum Control System"
description: "Programming of the swing-up algorithm for a cart-mounted pendulum, and of the control of the system in both its equilibrium positions, using PID and LQR control algorithms for real-time stabilization. Implemented using an Arduino connected to a Simulink environment."
date: from 09-2024 to 02-2025
categories: [Arduino, Control, MATLAB]
featured: true   # Forces this project to appear at the very top of your main grid layout

# Static preview backup image for the main directory block
featured_image: "/assets/images/projects/pendulum/preview.jpg"

github_url: "https://github.com/yourusername/inverted-pendulum"
demo_url: "https://github.com/yourusername/inverted-pendulum"

# === MEDIA GALLERY ===
# This feeds your loop video directly into the project overview page template
gallery:
  - type: "video"
    file: "/assets/images/projects/pendulum/swingup.mp4"
    description: "LQR controller stabilizing the cart-pole system against manual disturbances."
  - type: "image"
    file: "/assets/images/projects/pendulum/preview.jpg"
    description: "System wiring schematic and custom PCB layout."
---

## Project Overview
This project focuses on balancing a cart-pole system utilizing closed-loop digital control. By measuring the angle of the pendulum and tracking the position of the motorized platform, algorithms dynamically calculate real-time voltage response to maintain upright equilibrium.

### Key Objectives
* Modeled system dynamics using Lagrangian mechanics.
* Implemented **Linear Quadratic Regulator (LQR)** state-space control logic.
* Built hardware tracking with a high-resolution quadrature encoder.