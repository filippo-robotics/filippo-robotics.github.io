---
layout: default
title: "4DOF Industrial Robotics Design"
description: "Mechanical design, trajectory optimization, and dynamic modeling of a 4DOF industrial manipulator using MATLAB and Simscape."
date: "03-2025 to 07-2025"
categories: [Robotics, MATLAB, Simscape]
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
          Developed at the Politecnico di Milano, this project involves the mechanical design and control of a 4-degree-of-freedom (4DOF) industrial robot. The work encompasses the entire design cycle, including workspace mapping, kinematic and dynamic modeling, and the optimization of trajectories for a specific pick-and-place task involving block manipulation.
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

    <!-- 6. RIGHT COLUMN: MEDIA -->
    <div class="case-study-media">
      
      <!-- Media Item 1: Robot CAD / Assembly Rendering -->
      <div class="media-item">
        <img src="/assets/images/projects/robotics/preview.png" alt="4DOF Robot Structure Assembly">
        <div class="media-caption">Complete assembly render of the 4 DOF robot.</div>
      </div>

      <!-- Media Item 2: Dynamic Simulation Video (Muted & Looping) -->
      <div class="media-item">
        <video autoplay loop muted playsinline>
          <source src="/assets/images/projects/robotics/sim.mp4" type="video/mp4">
          Your browser does not support the video tag.
        </video> 
        <div class="media-caption">Simscape simulation of the pick-and-place task, demonstrating obstacle avoidance via smooth LSPB and Spline trajectories.</div>
      </div>

      <!-- Media Item 3: Workspace Isotropy Plot -->
      <div class="media-item">
        <img src="/assets/images/projects/robotics/isotropy.png" alt="Workspace Isotropy Heatmap">
        <div class="media-caption">Workspace isotropy index heatmap, verifying optimal kinematic quality and movement fluidity across the robot's entire reach.</div>
      </div>

    </div>

  </div>
</div>