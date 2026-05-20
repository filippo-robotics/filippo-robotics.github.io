---
layout: default
title: "Inverted Pendulum Control System"
description: "Closed-loop digital control and swing-up algorithm for a cart-mounted pendulum utilizing LQR and PID algorithms."
date: "09-2024 to 02-2025"
categories: [Arduino, Control, MATLAB]
featured: true
featured_image: "/assets/images/projects/pendulum/preview.png"
---

<style>
  /* Page reset and clean typography for dark mode case study */
  .case-study-wrapper {
    max-width: 1200px;
    margin: 4rem auto;
    padding: 0 2rem;
    font-family: system-ui, -apple-system, sans-serif;
    color: #e0e0e0; /* Light grey text for dark background readability */
  }

  /* 1. Main Title - Minimal & Bold */
  .case-study-title {
    font-size: 2.8rem;
    font-weight: 800;
    margin-bottom: 3.5rem;
    color: #ffffff; /* Pure white for high contrast */
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
    margin-bottom: 3.5rem;
  }

  .case-study-text h2 {
    font-size: 1.5rem;
    font-weight: 700;
    margin-bottom: 1.2rem;
    color: #ffffff;
    text-transform: uppercase;
    letter-spacing: 0.5px;
    border-bottom: 2px solid #3498db; /* Light Blue section divider */
    padding-bottom: 0.5rem;
  }

  .case-study-text h3 {
    font-size: 1.2rem;
    font-weight: 600;
    margin-top: 1.5rem;
    margin-bottom: 0.5rem;
    color: #3498db; /* Light Blue for module subheadings */
  }

  .case-study-text p {
    font-size: 1.05rem;
    line-height: 1.7;
    color: #cccccc;
    margin-bottom: 1rem;
  }

  .case-study-text strong {
    color: #ffffff;
  }

  /* RIGHT COLUMN: Media (Sticky to stay visible) */
  .case-study-media {
    position: sticky;
    top: 6rem; /* Stays visible while scrolling the text */
    display: flex;
    flex-direction: column;
    gap: 2.5rem;
  }

  .media-item {
    background: #111;
    border: 2px solid #3498db; /* Light Blue stroke around media */
    border-radius: 6px;
    overflow: hidden;
    box-shadow: 0 4px 15px rgba(0,0,0,0.4);
  }

  .media-item img, .media-item video {
    width: 100%;
    height: auto;
    display: block;
  }

  .media-caption {
    padding: 0.8rem 1rem;
    font-size: 0.9rem;
    color: #bbbbbb;
    background: rgba(255, 255, 255, 0.05); /* Slight contrast for caption box */
    border-top: 1px solid #3498db; /* Light Blue divider above text */
    font-style: italic;
  }

  /* Responsive: Stack on smaller screens */
  @media (max-width: 950px) {
    .case-study-grid {
      grid-template-columns: 1fr;
    }
    .case-study-media {
      position: static; /* Removes sticky behavior on mobile */
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
          Conducted at Politecnico di Milano, this project focuses on the modeling and real-time control of a linear inverted pendulum. The core objective was stabilizing the system in both downward and upward equilibrium positions, alongside designing an energy-based swing-up maneuver. By bridging theoretical Lagrangian modeling with experimental parameter identification, advanced control and filtering strategies were developed and tested on physical hardware.
        </p>
      </section>

      <!-- 3. SYSTEM ARCHITECTURE -->
      <section>
        <h2>System Architecture</h2>
        <p><strong>Mechanical Setup:</strong> A motorized cart moving along a horizontal rail featuring two degrees of freedom: horizontal cart position and pendulum angle.</p>
        <p><strong>Hardware & Sensors:</strong> A DC motor provides linear driving force via PWM signals, while two high-resolution encoders track cart translation and pendulum rotation.</p>
        <p><strong>Mathematical Model:</strong> Nonlinear equations of motion were derived using Lagrangian energy properties to accurately map system dynamics and friction.</p>
        <p><strong>State-Space Control:</strong> The model was linearized around equilibrium points into a four-variable state-space representation (position, velocity, angle, angular velocity) for real-time digital feedback.</p>
      </section>

      <!-- 4. IMPLEMENTATION BREAKDOWN -->
      <section>
        <h2>Implementation Breakdown</h2>
        
        <h3>Simulation & Parameter Identification</h3>
        <p>A Simscape virtual twin allowed risk-free optimization. Physical constants (masses, lengths, friction) were extracted experimentally via free decay oscillations and force interpolation.</p>

        <h3>Swing-Up & PID Control</h3>
        <p>An energy-based swing-up algorithm forces the pendulum from a stable downward position to the unstable upright position, where a PID controller provides initial feedback regulation.</p>

        <h3>LQR Control Strategy</h3>
        <p>An advanced Linear Quadratic Regulator (LQR) managed the interdependence between system states, calculating optimal gains to minimize a quadratic cost function for stabilization.</p>
        
        <h3>Signal Filtering (EKF)</h3>
        <p>To counteract severe measurement noise and encoder slippage, Low-Pass and Extended Kalman Filters (EKF) were implemented to achieve clean, reliable state estimation.</p>
      </section>

      <!-- 5. CONCLUSIONS -->
      <section>
        <h2>Conclusions</h2>
        <p>
          The system achieved precise downward control and successfully executed the swing-up maneuver in both simulation and lab testing. While PID feedback stabilized the upright position, the LQR controller faced hardware robustness challenges. Sensor noise, encoder slippage, and unmodeled nonlinearities introduced measurement bias, highlighting the critical impact of mechanical uncertainties on high-performance control systems.
        </p>
      </section>

    </div>

    <!-- 6. RIGHT COLUMN: MEDIA -->
    <div class="case-study-media">
      
      <!-- Media Item 1: Main Video -->
      <div class="media-item">
        <video autoplay loop muted playsinline>
          <source src="/assets/images/projects/pendulum/swingup.mp4" type="video/mp4">
        </video>
        <div class="media-caption">LQR controller stabilizing the cart-pole system against manual disturbances.</div>
      </div>

      <!-- Media Item 2: Architecture/Schematic Diagram -->
      <div class="media-item">
        <img src="/assets/images/projects/pendulum/preview.png" alt="System Architecture Diagram">
        <div class="media-caption">System wiring schematic and custom PCB layout.</div>
      </div>

    </div>

  </div>
</div>