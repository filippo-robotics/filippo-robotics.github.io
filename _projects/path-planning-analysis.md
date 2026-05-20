---
layout: default
title: "Comparative Analysis of Path Planning Algorithms"
description: "Implementation and benchmarking of A*, RRT, and RRT* path planning algorithms in complex 2D environments."
date: "09-2025 to 12-2025"
categories: [ROS, Path Planning, Algorithms]
featured: false
featured_image: "/assets/images/projects/planning/preview.png"
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
          Developed at the Politecnico di Milano, this project focuses on the implementation and benchmarking of advanced path planning algorithms, specifically A*, RRT (Rapidly-exploring Random Tree), and RRT*. The objective was to evaluate their performance in navigating complex 2D environments while balancing the trade-offs between computational speed and path optimality.
        </p>
      </section>

      <!-- SYSTEM ARCHITECTURE -->
      <section>
        <h2>System Architecture</h2>
        
        <div class="spec-item">
          <span class="spec-title">Simulation Framework:</span>
          <p class="spec-desc">The algorithms were tested and validated within a high-fidelity environment utilizing ROS and Gazebo to simulate realistic robotic movement and complex geometric constraints.</p>
        </div>

        <div class="spec-item">
          <span class="spec-title">Probabilistic vs. Deterministic Search:</span>
          <p class="spec-desc">The system architecture contrasts probabilistic sampling-based exploration (RRT/RRT*) with systematic grid-based search (A*).</p>
        </div>

        <div class="spec-item">
          <span class="spec-title">Voronoi Bias:</span>
          <p class="spec-desc">The RRT-based components utilize Voronoi bias to naturally direct the search toward unexplored regions of the configuration space.</p>
        </div>
      </section>

      <!-- IMPLEMENTATION BREAKDOWN -->
      <section>
        <h2>Implementation Breakdown</h2>
        
        <div class="spec-item">
          <span class="spec-title">Path Planning Optimization:</span>
          <p class="spec-desc">A standard RRT was implemented for fast feasible path discovery, while RRT* was developed with Optimal Parent Selection and Rewiring to ensure asymptotic optimality.</p>
        </div>

        <div class="spec-item">
          <span class="spec-title">Octile Heuristic A*:</span>
          <p class="spec-desc">For grid-based navigation, the A* algorithm was optimized using an Octile distance heuristic, which was proven more efficient than Euclidean distance for 8-directional grid movement.</p>
        </div>

        <div class="spec-item">
          <span class="spec-title">Hyperparameter Validation:</span>
          <p class="spec-desc">The project involved testing various step sizes to find the optimal balance between exploration speed and collision-free precision.</p>
        </div>

        <div class="spec-item">
          <span class="spec-title">Collision Detection:</span>
          <p class="spec-desc">A robust check was integrated to verify that every tree extension and connection remained within the obstacle-free configuration space.</p>
        </div>
      </section>

      <!-- CONCLUSIONS -->
      <section>
        <h2>Conclusions</h2>
        <p>
          The comparison revealed that while RRT is superior for real-time applications where speed is a priority, A* and RRT* are necessary when minimizing path length is critical. Notably, RRT* demonstrated the ability to outperform A* in specific scenarios by avoiding the "staircase effect" found in discrete grid-based movements.
        </p>
      </section>

    </div>

 <!-- RIGHT COLUMN: MEDIA -->
    <div class="case-study-media">
      
      <!-- Media Item 1: Standard RRT Benchmark Trials -->
      <div class="media-item">
        <img src="/assets/images/projects/planning/preview.png" alt="Rapidly-exploring Random Tree Path Planning Results">
        <div class="media-caption">Standard RRT exploration topologies benchmarked across four complex 2D environment configurations.</div>
      </div>

      <!-- Media Item 2: Asymptotically Optimal RRT* Optimizations -->
      <div class="media-item">
        <img src="/assets/images/projects/planning/RRT.png" alt="RRT Star Asymptotically Optimal Path Planning Performance Maps">
        <div class="media-caption">Asymptotically optimal RRT* paths demonstrating smoother trajectories and active tree rewiring across identical test layouts.</div>
      </div>

    </div>

  </div>
</div>