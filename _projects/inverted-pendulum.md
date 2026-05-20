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
    margin-bottom: 1rem;
  }

  /* Title on Left, Text on Right Layout */
  .spec-list {
    display: grid;
    grid-template-columns: 1fr;
    gap: 1rem;
    margin-bottom: 1.5rem;
  }
  
  @media (min-width: 768px) {
    .spec-list {
      grid-template-columns: 220px 1fr;
      gap: 1.5rem;
    }
  }

  .spec-title {
    color: #3498db;
    font-weight: 600;
    font-size: 1.1rem;
    margin: 0;
    line-height: 1.5;
  }

  .spec-desc {
    margin: 0;
    color: #cccccc;
    line-height: 1.7;
    font-size: 1.05rem;
  }

  /* RIGHT COLUMN: Media (Sticky to stay visible) */
  .case-study-media {
    position: sticky;
    top: 8rem;
    align-self: start;
    display: flex;
    flex-direction: column;
    gap: 2.5rem;
  }

  /* Premium Media Styling */
  .media-item {
    background: transparent;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 10px 30px rgba(52, 152, 219, 0.15); 
    border: 1px solid rgba(52, 152, 219, 0.2);
  }

  .media-item img, .media-item video {
    width: 100%;
    height: auto;
    display: block;
  }

  /* Solid Light Blue Caption Bar */
  .media-caption {
    padding: 1rem 1.2rem;
    font-size: 0.95rem;
    color: #ffffff;
    background: #3498db;
    font-weight: 500;
    line-height: 1.4;
  }

  /* Responsive: Stack on smaller screens */
  @media (max-width: 950px) {
    .case-study-grid {
      grid-template-columns: 1fr;
    }
    .case-study-media {
      position: static;
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
        
        <div class="spec-list">
          <div class="spec-title">Mechanical Setup:</div>
          <div class="spec-desc">A motorized cart moving along a horizontal rail featuring two degrees of freedom: horizontal cart position and pendulum angle.</div>
        </div>

        <div class="spec-list">
          <div class="spec-title">Hardware & Sensors:</div>
          <div class="spec-desc">A DC motor provides linear driving force via PWM signals, while two high-resolution encoders track cart translation and pendulum rotation.</div>
        </div>

        <div class="spec-list">
          <div class="spec-title">Mathematical Model:</div>
          <div class="spec-desc">Nonlinear equations of motion were derived using Lagrangian energy properties to accurately map system dynamics and friction.</div>
        </div>

        <div class="spec-list">
          <div class="spec-title">State-Space Control:</div>
          <div class="spec-desc">The model was linearized around equilibrium points into a four-variable state-space representation (position, velocity, angle, angular velocity) for real-time digital feedback.</div>
        </div>
      </section>

      <!-- 4. IMPLEMENTATION BREAKDOWN -->
      <section>
        <h2>Implementation Breakdown</h2>
        
        <div class="spec-list">
          <div class="spec-title">Simulation & Modeling:</div>
          <div class="spec-desc">A Simscape virtual twin allowed risk-free optimization. Physical constants (masses, lengths, friction) were extracted experimentally via free decay oscillations and force interpolation.</div>
        </div>

        <div class="spec-list">
          <div class="spec-title">Swing-Up & PID Control:</div>
          <div class="spec-desc">An energy-based swing-up algorithm forces the pendulum from a stable downward position to the unstable upright position, where a PID controller provides initial feedback regulation.</div>
        </div>

        <div class="spec-list">
          <div class="spec-title">LQR Control Strategy:</div>
          <div class="spec-desc">An advanced Linear Quadratic Regulator (LQR) managed the interdependence between system states, calculating optimal gains to minimize a quadratic cost function for stabilization.</div>
        </div>

        <div class="spec-list">
          <div class="spec-title">Signal Filtering (EKF):</div>
          <div class="spec-desc">To counteract severe measurement noise and encoder slippage, Low-Pass and Extended Kalman Filters (EKF) were implemented to achieve clean, reliable state estimation.</div>
        </div>
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
      
      <!-- Media Item 1: Hardware Image -->
      <div class="media-item">
        <img src="/assets/images/projects/pendulum/preview.png" alt="Hardware Setup">
        <div class="media-caption">Physical motorized cart setup with dual encoders for real-time state measurement.</div>
      </div>

      <!-- Media Item 2: Math Equation Image -->
      <div class="media-item">
        <img src="/assets/images/projects/pendulum/motion-equation.png" alt="System Dynamics Equation">
        <div class="media-caption">Nonlinear system dynamics derived via Lagrangian mechanics in a 4-variable state-space.</div>
      </div>
      
      <!-- Media Item 3: Real-World Video -->
      <div class="media-item">
        <video autoplay loop muted playsinline>
          <source src="/assets/images/projects/pendulum/swingup.mp4" type="video/mp4">
        </video>
        <div class="media-caption">Lab demonstration of the energy-based swing-up to an LQR-stabilized equilibrium.</div>
      </div>
      
      <!-- Media Item 4: Simulation Video -->
      <div class="media-item">
        <video autoplay loop muted playsinline>
          <source src="/assets/images/projects/pendulum/swingup-sim.mp4" type="video/mp4">
        </video>
        <div class="media-caption">Simscape virtual twin validating the analytical model and control strategy.</div>
      </div>

    </div>

  </div>
</div>