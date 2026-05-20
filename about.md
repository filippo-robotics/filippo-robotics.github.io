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
    margin-bottom: 2rem;
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

  /* Side-by-Side Image Gallery Layout at the bottom */
  .about-gallery-grid {
    display: grid;
    grid-template-columns: 1fr 1fr; /* 50/50 split matching layouts */
    gap: 2rem;
    margin-top: 2rem;
  }

  /* Premium Image Frame matching your project case studies */
  .about-gallery-item {
    background: transparent;
    border-radius: 15px; /* Softer, rounded look */
    overflow: hidden;
    border: 2px solid #3498db; /* Solid light blue stroke */
    box-shadow: 0 10px 30px rgba(52, 152, 219, 0.1);
  }

  .about-gallery-item img {
    width: 100%;
    height: auto;
    display: block;
    object-fit: cover;
  }

  /* Responsive Adjustments: Stack columns cleanly on mobile devices */
  @media (max-width: 600px) {
    .bio-split-grid,
    .about-gallery-grid {
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
      <p>
        I am a Mechanical Engineer specializing in Mechatronics and Robotics, graduated from Politecnico di Milano with a final grade of 110/110 (GPA 4.0/4.0). I enjoy working in collaborative environments and have a strong passion for robotics, automation, and intelligent systems engineering.
      </p>
      <p>
        My primary technical interests lie in the design and intelligent control of advanced robotic systems, particularly biomedical devices and exoskeletons engineered to restore and enhance independent autonomy for individuals with impaired mobility.
      </p>
      <p>
        I am also strongly interested in anthropomorphic robotics, autonomous navigation, and the development of complex robotic systems for industrial automation applications.
      </p>
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

    <!-- SIDE-BY-SIDE IMAGE GALLERY SECTION -->
    <section>
      <h2>Gallery</h2>
      <div class="about-gallery-grid">
        
        <!-- Image 1 -->
        <div class="about-gallery-item">
          <img src="{{ '/assets/images/aboutme1.png' | relative_url }}" alt="About Me Snapshot 1">
        </div>

        <!-- Image 2 -->
        <div class="about-gallery-item">
          <img src="{{ '/assets/images/aboutme2.png' | relative_url }}" alt="About Me Snapshot 2">
        </div>

      </div>
    </section>

  </div>
</div>