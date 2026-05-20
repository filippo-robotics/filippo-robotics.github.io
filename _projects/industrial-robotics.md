---
layout: default
title: "Mechanical design of a 4DOF robot"
description: "Mechanical design, trajectory optimization, and dynamic modeling of a 4DOF industrial manipulator using MATLAB and Simscape."
date: "03-2025 to 07-2025"
categories: [Robotics, MATLAB, Design]
featured: true
featured_image: "/assets/images/projects/robotics/preview.png"
---

<style>
  /* Page reset and clean typography for dark mode case study */
  .case-study-wrapper {
    max-width: 1200px;
    margin: 8rem auto 4rem auto;
    padding: 0 2rem;
    font-family: system-ui, -apple-system, sans-serif;
    color: #e0e0e0;
  }

  /* 1. Main Title - Minimal & Bold */
  .case-study-title {
    font-size: 2.8rem;
    font-weight: 800;
    margin-bottom: 3.5rem;
    color: #ffffff;
    border: none;
    padding: 0;
    line-height: 1.2;
  }

  /* 2-Column Layout Grid */
  .case-study-grid {
    display: grid;
    grid-template-columns: 1fr 1fr; /* 50/50 split */
    gap: 4rem;
    align-items: start;
  }

  /* LEFT COLUMN: Text Content */
  .case-study-text section {
    margin-bottom: 4rem;
  }

  .case-study-text h2 {
    font-size: 1.5rem;
    font-weight: 700;
    margin-bottom: 2rem;
    color: #ffffff;
    text-transform: uppercase;
    letter-spacing: 0.5px;
    border-bottom: 2px solid #3498db; /* Light Blue section divider */
    padding-bottom: 0.5rem;
  }

  .case-study-text p {
    font-size: 1.05rem;
    line-height: 1.7;
    color: #cccccc;
    margin-bottom: 1.5rem;
  }

  /* Classical Paragraph Layout for Specs */
  .spec-item {
    margin-bottom: 1.8rem;
  }

  .spec-title {
    color: #3498db; /* Light Blue Title */
    font-weight: 600;
    font-size: 1.1rem;
    display: block; /* Pushes text underneath like a classical paragraph */
    margin-bottom: 0.4rem;
  }

  .spec-desc {
    margin: 0;
    color: #cccccc;
    line-height: 1.7;
    font-size: 1.05rem;
  }

  /* RIGHT COLUMN: Media (Scrolls normally with the page) */
  .case-study-media {
    display: flex;
    flex-direction: column;
    gap: 2.5rem;
  }

  /* Premium Media Styling with 15px Rounded Corners & Light Blue Stroke */
  .media-item {
    background: transparent;
    border-radius: 15px; /* Softer, rounded look */
    overflow: hidden;
    border: 2px solid #3498db; /* Solid light blue stroke */
    box-shadow: 0 10px 30px rgba(52, 152, 219, 0.1); 
  }

  .media-item img, .media-item video {
    width: 100%;
    height: auto;
    display: block;
    border-top-left-radius: 13px; /* Prevent image bleed outside border */
    border-top-right-radius: 13px;
  }

  /* Placeholder Style for items waiting for final media assets */
  .media-placeholder {
    width: 100%;
    aspect-ratio: 16 / 9;
    background: rgba(52, 152, 219, 0.05);
    display: flex;
    align-items: center;
    justify-content: center;
    color: #3498db;
    font-weight: 500;
    border-top-left-radius: 13px;
    border-top-right-radius: 13px;
    border-bottom: 1px solid rgba(52, 152, 219, 0.2);
  }

  /* Premium Semi-Transparent Caption Bar */
  .media-caption {
    padding: 1.2rem;
    font-size: 0.95rem;
    color: #e0e0e0;
    background: rgba(20, 25, 35, 0.85); /* Deep elegant backdrop */
    border-top: 1px solid rgba(52, 152, 219, 0.2);
    font-weight: 500;
    line-height: 1.5;
  }

  /* Responsive: Stack on smaller screens */
  @media (max-width: 950px) {
    .case-study-grid {
      grid-template-columns: 1fr;
      gap: 2rem;
    }
  }
</style>

<div class="case-study-wrapper">
  
  <!-- 1. PROJECT TITLE -->
  <h1 class="case-study-title">{{ page.title }}</h1>

  <div class="case-study-grid">
    
    <!-- LEFT COLUMN: TEXT CONTENT -->
    <div class="case-study-text">
      
      <!-- 2. PROJECT OVERVIEW -->
      <section>
        <h2>Project Overview</h2>
        <p>
          Developed at Politecnico di Milano in collaboration with University of Pavia, this project involves the mechanical design and control of a 4-degree-of-freedom (4DOF) industrial robot. The work encompasses the entire design cycle, including workspace mapping, kinematic and dynamic modeling, and the optimization of trajectories for a specific pick-and-place task involving block manipulation.
        </p>
      </section>

      <!-- 3. SYSTEM ARCHITECTURE -->
      <section>
        <h2>System Architecture</h2>
        
        <div class="spec-item">
          <span class="spec-title">Manipulator Configuration:</span>
          <p class="spec-desc">A 4DOF system featuring three revolute joints and one prismatic joint for vertical (z-axis) movement.</p>
        </div>

        <div class="spec-item">
          <span class="spec-title">Mechanical Balancing:</span>
          <p class="spec-desc">A counterweight system was integrated into the fourth joint to balance the static gravitational force of the robot’s components, minimizing actuator effort.</p>
        </div>

        <div class="spec-item">
          <span class="spec-title">Drive System:</span>
          <p class="spec-desc">The architecture utilizes motors with specific transmission ratios (K=9 for revolute, K=5 for prismatic) to meet the required torque and velocity demands.</p>
        </div>

        <div class="spec-item">
          <span class="spec-title">Simulation Environment:</span>
          <p class="spec-desc">The system was fully modeled using Simscape and MATLAB to validate the mechanical structure and control logic before implementation.</p>
        </div>
      </section>

      <!-- 4. IMPLEMENTATION BREAKDOWN -->
      <section>
        <h2>Implementation Breakdown</h2>
        
        <div class="spec-item">
          <span class="spec-title">Kinematic Modeling:</span>
          <p class="spec-desc">Inverse kinematics were solved numerically using the fmincon function in MATLAB, which minimizes the distance error between the end-effector and target points while respecting joint constraints.</p>
        </div>

        <div class="spec-item">
          <span class="spec-title">Trajectory Planning:</span>
          <p class="spec-desc">Complex paths were developed by selecting intermediate points to avoid obstacles. These points were smoothed using two interpolation methods: Lines and Parabolas (LAP) and Cubic Splines.</p>
        </div>

        <div class="spec-item">
          <span class="spec-title">Dynamic Analysis:</span>
          <p class="spec-desc">A full dynamic model was derived using a Lagrangian approach, incorporating Jacobian matrices to calculate required torques for each motor during the task.</p>
        </div>

        <div class="spec-item">
          <span class="spec-title">Performance Validation:</span>
          <p class="spec-desc">Calculated torques were compared against the HG-MR23 motor performance curves to ensure that all maneuvers remained within the continuous running range.</p>
        </div>
      </section>

      <!-- 5. CONCLUSIONS -->
      <section>
        <h2>Conclusions</h2>
        <p>
          The project successfully demonstrated a validated mechanical design capable of executing high-precision tasks. The results showed a high degree of correlation between the analytical MATLAB calculations and the Simscape physical simulations. By confirming that all motor torques and velocities stayed within safety limits, the design proved to be both mechanically robust and operationally feasible for industrial applications.
        </p>
      </section>

    </div>

    <!-- 6. RIGHT COLUMN: MEDIA PLACEHOLDERS -->
    <div class="case-study-media">
      
      <!-- Media Item 1: Robot CAD / Assembly Rendering -->
      <div class="media-item">
        <div class="media-placeholder">[ Image Placeholder: Robot Mechanical Assembly ]</div>
        <!-- Once ready, replace the line above with: <img src="/assets/images/projects/robotics/cad-model.png" alt="4DOF Robot Structure"> -->
        <div class="media-caption">Full mechanical assembly of the 4DOF manipulator featuring three revolute joints and an integrated counterweight system.</div>
      </div>

      <!-- Media Item 2: Trajectory Planning Plots -->
      <div class="media-item">
        <div class="media-placeholder">[ Image Placeholder: Trajectory Curves ]</div>
        <!-- Once ready, replace the line above with: <img src="/assets/images/projects/robotics/trajectory.png" alt="Trajectory Interpolation Curves"> -->
        <div class="media-caption">Comparison profiles of the Lines and Parabolas (LAP) algorithm versus Cubic Splines during obstacle avoidance routines.</div>
      </div>
      
      <!-- Media Item 3: Dynamic Simulation Video -->
      <div class="media-item">
        <div class="media-placeholder">[ Video Placeholder: Simscape Pick and Place ]</div>
        <!-- Once ready, replace the line above with:
        <video autoplay loop muted playsinline>
          <source src="/assets/images/projects/robotics/pick-place-sim.mp4" type="video/mp4">
        </video> 
        -->
        <div class="media-caption">Real-time Simscape physical twin executing block handling loops and torque limit validations.</div>
      </div>
      
      <!-- Media Item 4: Motor Performance Verification Curve -->
      <div class="media-item">
        <div class="media-placeholder">[ Image Placeholder: HG-MR23 Motor Limits ]</div>
        <!-- Once ready, replace the line above with: <img src="/assets/images/projects/robotics/motor-limits.png" alt="Motor Torque Curves"> -->
        <div class="media-caption">Analytical motor torque trajectories mapped safely inside the continuous running zones of the HG-MR23 curves.</div>
      </div>

    </div>

  </div>
</div>