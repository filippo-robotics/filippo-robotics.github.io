---
layout: project
title: "Simulation-Informed Human-in-the Loop Optimization for Supernumerary Robotic Assistance in Activities of Daily Living"
description: "I worked in Prof. Patrick Slade’s lab on a robotic exoskeleton project aimed at assisting people with motor impairments and the elderly. My contribution..."
date: 2026-05-19
categories: [Robotics, Biomechanics, Machine Learning, Exoskeletons]
featured: false # Keep this false so it doesn't accidentally duplicate in the lower 3-project grid!
featured_image: "/assets/images/projects/thesis/featured.jpg"
---

<style>
  /* Premium Light Blue Academic Publication Banner */
  .publication-notice-banner {
    display: flex;
    align-items: center;
    gap: 1.5rem;
    margin-top: 5rem;
    padding: 1.5rem 2rem;
    background: rgba(52, 152, 219, 0.05); /* Soft, translucent light blue */
    border-left: 4px solid #3498db; /* Signature solid blue indicator */
    border-radius: 4px 15px 15px 4px; /* Matches 15px card roundness gracefully */
    box-shadow: 0 4px 20px rgba(0, 0, 0, 0.15);
  }

  .notice-icon-wrapper {
    display: flex;
    align-items: center;
    justify-content: center;
    background: rgba(52, 152, 219, 0.12);
    padding: 0.75rem;
    border-radius: 10px;
  }

  .notice-text-content {
    display: flex;
    flex-direction: column;
    gap: 0.3rem;
  }

  .notice-badge {
    font-size: 0.75rem;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 1px;
    color: #3498db;
  }

  .notice-message {
    margin: 0 !important; /* Forces layout tracking inside wrapper grids */
    font-size: 1.05rem;
    line-height: 1.5;
    color: #e0e0e0;
  }

  .notice-message strong {
    color: #ffffff;
    font-weight: 600;
  }

  /* Smooth stacking transformation for mobile viewpoints */
  @media (max-width: 600px) {
    .publication-notice-banner {
      flex-direction: column;
      align-items: flex-start;
      gap: 1rem;
      padding: 1.5rem;
    }
  }
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

  /* RIGHT COLUMN: Media */
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
  
  <h1 class="case-study-title">{{ page.title }}</h1>

  <div class="case-study-grid">
    
    <!-- LEFT COLUMN: TEXT CONTENT -->
    <div class="case-study-text">
      
      <!-- ABSTRACT & OBJECTIVE -->
      <section>
        <h2>Thesis Abstract & Research Objective</h2>
        <p>
          This thesis addresses the "sim-to-real gap" in assistive robotics by developing a task-agnostic Supernumerary Robotic Limb (SRL) system. The research objective was to create a framework that combines biomechanical simulations with Human-in-the-Loop Optimization (HILO) to provide personalized assistance for multiple Activities of Daily Living (ADLs), specifically sit-to-stand, stair climbing, and object lifting. The system aims to minimize user fatigue and muscle activation, enhancing autonomy for individuals with mobility impairments.
        </p>
      </section>

      <!-- SYSTEM ARCHITECTURE -->
      <section>
        <h2>System Architecture & Hardware Design</h2>
        
        <div class="spec-item">
          <span class="spec-title">Mechanical Structure:</span>
          <p class="spec-desc">The hardware features a custom adjustable vest with a carbon fiber two-link robotic arm. It utilizes two high-torque brushless DC motors (AK70-10 and AK60-6) controlled via a CAN interface.</p>
        </div>

        <div class="spec-item">
          <span class="spec-title">Sensor Fusion:</span>
          <p class="spec-desc">A wired IMU provides stable real-time phase estimation, while Delsys EMG sensors measure physiological muscle activity.</p>
        </div>

        <div class="spec-item">
          <span class="spec-title">End-Effector Innovation:</span>
          <p class="spec-desc">A new 3D-printed degree of freedom (wrist rotation) was designed in PLA-CF to allow the gripper to follow natural human motion more smoothly during complex tasks.</p>
        </div>

        <div class="spec-item">
          <span class="spec-title">Communication Setup:</span>
          <p class="spec-desc">A Raspberry Pi acts as the onboard computer, coordinating motor control and sensor data via an SSH connection to a host workstation.</p>
        </div>
      </section>

      <!-- METHODOLOGY -->
      <section>
        <h2>Advanced Methodology: Simulation-Informed HILO</h2>
        
        <div class="spec-item">
          <span class="spec-title">Biomechanical Modeling:</span>
          <p class="spec-desc">Utilizing OpenCap and OpenSim Moco, personalized musculoskeletal models were generated from unassisted motion data to identify an "initial guess" for assistive force profiles.</p>
        </div>

        <div class="spec-item">
          <span class="spec-title">Real-time Phase Estimation:</span>
          <p class="spec-desc">A Support Vector Regression (SVR) model was trained to map kinematic IMU data to a monotonic 0–100% motion phase, enabling precise timing of assistance.</p>
        </div>

        <div class="spec-item">
          <span class="spec-title">Optimization Framework:</span>
          <p class="spec-desc">A Bayesian Optimization algorithm iteratively refined five force parameters (peak time, peak force, fall time) based on real-time EMG feedback.</p>
        </div>

        <div class="spec-item">
          <span class="spec-title">Motion Segmentation:</span>
          <p class="spec-desc">The Angular Rate Energy Detector (ARED) method was implemented to automatically distinguish active movement from rest intervals.</p>
        </div>
      </section>

      <!-- EXPERIMENTAL RESULTS -->
      <section>
        <h2>Experimental Results & Validation</h2>
        
        <div class="spec-item">
          <span class="spec-title">Muscle Activation Reduction:</span>
          <p class="spec-desc">Validation on five participants demonstrated significant average reductions in target muscle activity: -11% for sit-to-stand, -18% for object lifting, and -17% for stair step-up.</p>
        </div>

        <div class="spec-item">
          <span class="spec-title">Personalization Efficacy:</span>
          <p class="spec-desc">The results confirmed that optimal assistance parameters vary uniquely by individual, proving that HILO is essential for surpassing the limitations of generalized simulation-based models.</p>
        </div>

        <div class="spec-item">
          <span class="spec-title">Stability & Convergence:</span>
          <p class="spec-desc">The optimization landscape showed a single dominant optimum, with the process typically stabilizing within 80 iterations, reducing experimental time and user fatigue.</p>
        </div>
      </section>

      <!-- CONCLUSIONS -->
      <section>
        <h2>Academic Conclusions & Future Work</h2>
        <p>
          The thesis successfully establishes a generalized pipeline for biomechanically informed robotic assistance that is effective across diverse tasks without mechanical redesign. While current results are promising, future developments will focus on reducing hardware weight to further improve efficiency compared to the "no-exoskeleton" condition. The framework provides a foundation for fully task-agnostic platforms that could eventually support cyclic activities like walking through deep learning-based predictive control.
        </p>
      </section>

    </div>

    <!-- RIGHT COLUMN: MEDIA -->
    <div class="case-study-media">
      
      <!-- Media Item 1: Home Page Loop Video Showcase -->
      <div class="media-item">
        <video autoplay loop muted playsinline preload="auto" poster="{{ '/assets/images/projects/thesis/featured.jpg' | relative_url }}">
          <source src="{{ '/assets/images/projects/thesis/demo.mp4' | relative_url }}" type="video/mp4">
          Your browser does not support the video tag.
        </video>
        <div class="media-caption">Dynamic system demonstration of the Supernumerary Robotic Limb executing assistive task profiles.</div>
      </div>

      <!-- Media Item 2: Mechanical and Communication Infrastructure Diagram -->
      <div class="media-item">
        <img src="/assets/images/projects/thesis/system.png" alt="SRL Mechanical Architecture and Embedded Communication Diagram">
        <div class="media-caption">System architecture mapping the brushless DC motor actuators, sensor network integrations, and workstation communication setup.</div>
      </div>

      <!-- Media Item 3: Operational Tasks and Kinematic Frames Diagram -->
      <div class="media-item">
        <img src="/assets/images/projects/thesis/tasks.png" alt="Activities of Daily Living Tasks and Kinematic Frame Comparisons">
        <div class="media-caption">Operational ADL tasks showcasing the structural comparison between the user's reference frame (red) and the SRL reference frame (pink) used for Jacobian calculation.</div>
      </div>

    </div>

  </div>

  
 
</div>
