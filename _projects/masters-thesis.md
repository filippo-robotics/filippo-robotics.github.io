---
layout: project
title: "Simulation-Informed Human-in-the Loop Optimization for Supernumerary Robotic Assistance in Activities of Daily Living"
description: "I worked in Prof. Patrick Slade’s lab on a robotic exoskeleton project aimed at assisting people with motor impairments and the elderly. My contribution..."
date: 2026-05-19
categories: [Robotics, Biomechanics, Machine Learning, Exoskeletons]
featured: false # Keep this false so it doesn't accidentally duplicate in the lower 3-project grid!

# The image shown inside the thesis project page
featured_image: "/assets/images/projects/thesis/featured.jpg"

github_url: "https://github.com/yourusername/thesis-repo"
demo_url: "https://youtu.be/your-thesis-demo"

# If you have a 3D CAD model of your thesis project
models:
  - file: "/assets/models/thesis/robot_model.gltf"
    description: "Full assembly of the mechatronic testing rig"

# If you want to show your circuit diagrams
schematics:
  - file: "/assets/schematics/thesis/hardware_circuit.png"
    description: "Custom PCB layout for sensor data acquisition"

# You can paste an important snippet of your control algorithms here
code_files:
  - name: "Trajectory Optimization"
    file: "trajectory_planner.py"
    language: "python"
    download_url: "https://github.com/yourusername/your-repo/blob/main/trajectory_planner.py"
    content: |
      import numpy as np
      
      def optimize_path(start, goal):
          # Your thesis mathematical solver code goes here
          print("Optimizing trajectory...")
          return True

# Bill of Materials used in your thesis rig
components:
  - name: "Microcontroller / FPGA Board"
    quantity: 1
    description: "Main controller processing the kinematics loop"
    link: "https://example.com"

# Gallery for your thesis defense slides, photos in the lab, or performance graphs
gallery:
  - type: "video"
    file: "/assets/images/projects/thesis/demo.mp4"
    description: "Robot in action - Full demonstration video"
  - type: "image"
    file: "/assets/images/projects/thesis/featured.jpg"
    description: "Close-up profile of the hardware assembly"
---

## Thesis Abstract
Write a summary of your thesis here. What was the core academic or engineering problem you tackled? What were your key contributions or findings?

## Methodology & Hardware Architecture
Describe the physical mechatronic system you built or analyzed. Mention your mechanical design, structural choices, and electronic component selection.

## Control Algorithms & Software
Explain the mathematics, physics equations, or programming architecture (like ROS packages, inverse kinematics solvers, or computer vision tracking) you implemented.

## Experimental Results
Detail how the system performed during testing. (If you have data plots or performance graphs, you can talk about them here!)