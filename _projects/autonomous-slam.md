---
layout: default
title: "Turtlebot3 Autonomous Driving"
description: "An autonomous indoor mapping and navigation pipeline using TurtleBot3, gmapping, and optimized sparse A* algorithms."
date: "01-2026 to 05-2026"
categories: [Gazebo, Autonomous Navigation, ROS]
featured: true
featured_image: "/assets/images/projects/slam/preview.png"
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
      
      <!-- PROJECT OVERVIEW -->
      <section>
        <h2>Project Overview</h2>
        <p>
          This project demonstrates a complete autonomous pipeline for indoor exploration, mapping (SLAM), and navigation using a TurtleBot3 Waffle Pi. The system was designed to explore an unknown environment, reconstruct a full occupancy grid map, and execute autonomous path planning to reach specified goal coordinates.
        </p>
      </section>

      <!-- SYSTEM ARCHITECTURE -->
      <section>
        <h2>System Architecture</h2>
        
        <div class="spec-item">
          <span class="spec-title">ROS Middleware:</span>
          <p class="spec-desc">The entire software pipeline is integrated within the ROS framework, coordinating the communication between the slam_gmapping node, sensor topics (/scan, /odom), and the navigation controller.</p>
        </div>

        <div class="spec-item">
          <span class="spec-title">Gazebo Simulation:</span>
          <p class="spec-desc">High-fidelity testing and validation were conducted in Gazebo using the house.launch environment, which provides a realistic residential space for autonomous exploration.</p>
        </div>

        <div class="spec-item">
          <span class="spec-title">Visualization & Sensors:</span>
          <p class="spec-desc">The architecture utilizes an onboard LiDAR sensor for environment reconstruction, with RViz serving as the primary interface for real-time visualization of the evolving occupancy grid.</p>
        </div>
      </section>

      <!-- IMPLEMENTATION BREAKDOWN -->
      <section>
        <h2>Implementation Breakdown</h2>
        
        <div class="spec-item">
          <span class="spec-title">SLAM & Full Map Reconstruction:</span>
          <p class="spec-desc">A complete map of the simulated house was generated using the ROS gmapping package while manually driving the robot via a teleop node.</p>
        </div>

        <div class="spec-item">
          <span class="spec-title">Large-Scale Sparse A*:</span>
          <p class="spec-desc">The A* planner was optimized to handle high-resolution 384x384 maps by implementing sparse adjacency matrices, reducing the memory footprint from billions of potential elements to just 1.2 million non-zero entries.</p>
        </div>

        <div class="spec-item">
          <span class="spec-title">Map Inflation:</span>
          <p class="spec-desc">For safety, obstacles were expanded through morphological erosion with a disk-shaped structuring element, ensuring the robot maintains a safe clearance from walls.</p>
        </div>

        <div class="spec-item">
          <span class="spec-title">Incremental Replanning:</span>
          <p class="spec-desc">A closed-loop navigation strategy was developed where the A* planner is periodically re-invoked as the map is updated, allowing the robot to adapt its trajectory to newly discovered obstacles in real-time.</p>
        </div>
      </section>

      <!-- CONCLUSIONS -->
      <section>
        <h2>Conclusions</h2>
        <p>
          The project successfully achieved precise autonomous navigation across multiple test pairs, with the robot reaching all goals while maintaining safe distances from obstacles. The Incremental Replanning approach proved highly robust, showing that the system could effectively correct its path as it gained more information about the environment.
        </p>
      </section>

    </div>

 <!-- RIGHT COLUMN: MEDIA -->
    <div class="case-study-media">
      
      <!-- Media Item 1: Gazebo Environment Simulation Preview -->
      <div class="media-item">
        <img src="/assets/images/projects/slam/preview.png" alt="TurtleBot3 inside Gazebo Residential House Simulation">
        <div class="media-caption">Gazebo house environment simulation featuring the TurtleBot3 Waffle Pi robot configuring initial indoor sensor parameters.</div>
      </div>

      <!-- Media Item 2: Global A* Path Planning Mapping Trace -->
      <div class="media-item">
        <img src="/assets/images/projects/slam/global-planning.png" alt="Global A Star Path Planning Trajectory Plot">
        <div class="media-caption">Optimal collision-free global path determined using the memory-optimized Sparse A* search algorithm.</div>
      </div>

    </div>

  </div>
</div>