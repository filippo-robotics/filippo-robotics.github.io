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
  /* Page reset and clean typography for case study */
  .case-study-wrapper {
    max-width: 1200px;
    margin: 4rem auto;
    padding: 0 2rem;
    font-family: system-ui, -apple-system, sans-serif;
    color: #333;
  }

  /* 1. Main Title - Minimal & Bold */
  .case-study-title {
    font-size: 2.8rem;
    font-weight: 800;
    margin-bottom: 3.5rem;
    color: #111;
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
    color: #111;
    text-transform: uppercase;
    letter-spacing: 0.5px;
    border-bottom: 2px solid #eaeaea;
    padding-bottom: 0.5rem;
  }

  .case-study-text h3 {
    font-size: 1.2rem;
    font-weight: 600;
    margin-top: 1.5rem;
    margin-bottom: 0.5rem;
    color: #333;
  }

  .case-study-text p {
    font-size: 1.05rem;
    line-height: 1.7;
    color: #444;
    margin-bottom: 1rem;
  }

  .case-study-text strong {
    color: #111;
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
    background: #fdfdfd;
    border: 1px solid #eaeaea;
    border-radius: 6px;
    overflow: hidden;
    box-shadow: 0 4px 12px rgba(0,0,0,0.03);
  }

  .media-item img, .media-item video {
    width: 100%;
    height: auto;
    display: block;
  }

  .media-caption {
    padding: 0.8rem 1rem;
    font-size: 0.9rem;
    color: #555;
    background: #fff;
    border-top: 1px solid #eaeaea;
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
          [Insert 5-6 lines abstract here. Explain what the project is, the core problem it solves (e.g., non-linear system stabilization), and the high-level approach (e.g., LQR control via Arduino and MATLAB/Simulink).]
        </p>
      </section>

      <!-- 3. SYSTEM ARCHITECTURE -->
      <section>
        <h2>System Architecture</h2>
        <p><strong>Mechanical System:</strong> [Describe cart, track, pendulum rod, and physics/dynamics constraints]</p>
        <p><strong>Electronics / Hardware:</strong> [Describe Arduino, motor drivers, quadrature encoders, power delivery]</p>
        <p><strong>Software / Control Logic:</strong> [Describe MATLAB/Simulink interface, real-time data acquisition, control loop frequency]</p>
        <p><strong>System Interaction:</strong> [Explain the data flow from encoder -> Arduino -> MATLAB -> Motor Driver -> Actuator]</p>
      </section>

      <!-- 4. IMPLEMENTATION BREAKDOWN -->
      <section>
        <h2>Implementation Breakdown</h2>
        
        <h3>Control System (LQR & PID)</h3>
        <p>[2-4 lines: What it does, why it exists, how it contributes. E.g., State-space LQR logic for upright stabilization and PID for swing-up.]</p>

        <h3>Sensor Feedback System</h3>
        <p>[2-4 lines: What it does, why it exists, how it contributes. E.g., High-resolution quadrature encoding to track pendulum angle and cart position with near-zero latency.]</p>

        <h3>Embedded Logic (Arduino)</h3>
        <p>[2-4 lines: What it does, why it exists, how it contributes. E.g., Handles hardware interrupts for encoder reading and translates PWM signals to the motor driver.]</p>
        
        <h3>Actuation System</h3>
        <p>[2-4 lines: What it does, why it exists, how it contributes. E.g., DC motor with belt drive translating rotational torque into linear cart acceleration.]</p>
      </section>

    </div>

    <!-- 5. RIGHT COLUMN: MEDIA -->
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