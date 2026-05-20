---
layout: default
title: "About Me"
permalink: /about/
---

<style>
  /* Base wrapper matching premium dark mode project layouts */
  .about-me-wrapper {
    max-width: 850px; /* Clean single-column readability width */
    margin: 8rem auto 4rem auto;
    padding: 0 2rem;
    font-family: system-ui, -apple-system, sans-serif;
    color: #e0e0e0;
  }

  /* Main Title - Minimal & Bold */
  .about-me-title {
    font-size: 2.8rem;
    font-weight: 800;
    margin-bottom: 3.5rem;
    color: #ffffff;
    border: none;
    padding: 0;
    line-height: 1.2;
  }

  /* Section Structural Layouts */
  .about-me-text section {
    margin-bottom: 4rem;
  }

  .about-me-text h2 {
    font-size: 1.5rem;
    font-weight: 700;
    margin-bottom: 2rem;
    color: #ffffff;
    text-transform: uppercase;
    letter-spacing: 0.5px;
    border-bottom: 2px solid #3498db; /* Solid Light Blue section divider */
    padding-bottom: 0.5rem;
  }

  .about-me-text p {
    font-size: 1.05rem;
    line-height: 1.7;
    color: #cccccc;
    margin-bottom: 1.5rem;
  }

  /* Classical Paragraph Layout for Specs and Details */
  .bio-spec-item {
    margin-bottom: 1.8rem;
  }

  .bio-spec-title {
    color: #3498db; /* Light Blue Sub-Title Heading */
    font-weight: 600;
    font-size: 1.1rem;
    display: block; 
    margin-bottom: 0.4rem;
  }

  .bio-spec-desc {
    margin: 0;
    color: #cccccc;
    line-height: 1.7;
    font-size: 1.05rem;
  }

  /* 2-Column Split specifically for Language and Skill blocks */
  .bio-split-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 2rem;
  }

  @media (max-width: 600px) {
    .bio-split-grid {
      grid-template-columns: 1fr;
      gap: 1.5rem;
    }
  }
</style>

<div class="about-me-wrapper">
  
  <h1 class="about-me-title">About Me</h1>

  <div class="about-me-text">
    
    <!-- PROFESSIONAL SUMMARY -->
    <section>
      <h2>Professional Profile</h2>
      <p>
        I am a Mechanical Engineer specializing in Mechatronics and Robotics, graduated from Politecnico di Milano with a final grade of 110/110 (GPA 4.0/4.0). I am highly motivated, thrive in collaborative team environments, and hold a deep professional passion for robotics and automation engineering fields.
      </p>
      <p>
        My primary technical interests lie in the design and intelligent control of advanced robotic systems, particularly biomedical devices, physical interfaces, and supernumerary exoskeletons engineered to restore and enhance independent autonomy for individuals with impaired mobility.
      </p>
    </section>

    <!-- EXPERIENCE & RESEARCH HIGHLIGHTS -->
    <section>
      <h2>Research & Industry Milestones</h2>
      
      <div class="bio-spec-item">
        <span class="bio-spec-title">Harvard University — Master's Research</span>
        <p class="bio-spec-desc">
          Completed my Master's Thesis research inside Prof. Patrick Slade’s laboratory, working directly on an advanced supernumerary robotic exoskeleton. My focus centered on designing and building a Machine Learning-based predictive control framework capable of assisting users across a diverse range of complex activities of daily living (ADLs).
        </p>
      </div>

      <div class="bio-spec-item">
        <span class="bio-spec-title">R4P S.r.l. — Robotics Engineer</span>
        <p class="bio-spec-desc">
          Currently working within the research and development division at R4P S.r.l. My day-to-day role involves enhancing complex control system stability loops and automating heavy industrial robotic applications, spanning automated factory production lines to intelligent autonomous mobile configurations.
        </p>
      </div>
    </section>

    <!-- COMPETENCIES & LANGUAGES -->
    <section>
      <h2>Languages & Communication</h2>
      <div class="bio-split-grid">
        
        <div class="bio-spec-item">
          <span class="bio-spec-title">Italian</span>
          <p class="bio-spec-desc">Mother tongue / Native proficiency.</p>
        </div>

        <div class="bio-spec-item">
          <span class="bio-spec-title">English</span>
          <p class="bio-spec-desc">Fluent professional proficiency (both written and spoken). First Certificate in English, certified at an Advanced C1 Level.</p>
        </div>

      </div>
    </section>

    <!-- PERSONAL INTERESTS -->
    <section>
      <h2>Interests & Activities</h2>
      
      <div class="bio-spec-item">
        <span class="bio-spec-title">Social Responsibility & Coordination</span>
        <p class="bio-spec-desc">Responsible for planning and organizing structural charity fundraising drives to support international aid programs led by the AVSI non-profit organization.</p>
      </div>

      <div class="bio-spec-item">
        <span class="bio-spec-title">Personal Pursuits</span>
        <p class="bio-spec-desc">Certified in basic, intermediate, and advanced levels of professional wine tasting. Outside the lab, I am an avid skier, fly fisherman, and enjoy capturing perspective aerial photography and cinematography utilizing custom drones.</p>
      </div>
    </section>

  </div>
</div>