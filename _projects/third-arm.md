---
layout: project
title: "Autonomous Robotic Arm"
description: "A 4-DOF mechatronic arm utilizing inverse kinematics and ROS for precision sorting."
date: 2026-05-19
categories: [Robotics, Mechatronics, ROS]
featured: true   # Set to true if you want it on your homepage grid!

# Main image displayed on the card (make sure to create this folder/file)
featured_image: "/assets/images/projects/robotic-arm/featured.jpg"

github_url: "https://github.com/yourusername/robotic-arm"
demo_url: "https://youtu.be/your-video-link"

# 3D CAD Models (Optional: delete if not using)
models:
  - file: "/assets/models/robotic-arm/model.gltf"
    description: "3D assembly of the gripper mechanism"

# Circuit Schematics (Optional: delete if not using)
schematics:
  - file: "/assets/schematics/robotic-arm/circuit.png"
    description: "Power distribution and microcontroller pinouts"

# Code Files to show off your programming (Optional)
code_files:
  - name: "Inverse Kinematics Solver"
    file: "kinematics.py"
    language: "python"
    download_url: "https://github.com/yourusername/robotic-arm/blob/main/kinematics.py"
    content: |
      import numpy as np
      
      def calculate_ik(x, y, z):
          # Your cool robotics code math goes here
          pass

# Bill of Materials / Components (Optional)
components:
  - name: "NEMA 17 Stepper Motor"
    quantity: 4
    description: "Joint actuators"
    link: "https://www.sparkfun.com"

# Gallery for pictures, GIFs, or gameplay/test videos
gallery:
  - type: "image"
    file: "/assets/images/projects/robotic-arm/testing.jpg"
    description: "Calibration phase testing"
  - type: "video"
    file: "/assets/images/projects/robotic-arm/demo.mp4"
    description: "Sorting routine at 2x speed"
---

## Project Overview
Write your project introduction here. Explain what problem your robot solves, your inspiration, and the final results. You can use standard markdown like **bold text** or lists.

## Mechanical Design
Detail your CAD layout, 3D printing choices, or structural materials used here.

## Electronics & Control
Explain your microcontroller choice, sensor integrations, and control loop tracking (e.g. PID tuning).