---
layout: default
---

<style>
  /* ========================================== */
  /* 1. HERO USER PROFILE SECTION STYLES        */
  /* ========================================== */
  
  /* Main container: Image on left, Text block on right */
  .hero-profile-layout {
    display: flex;
    flex-direction: row !important;
    align-items: center;
    justify-content: center;
    gap: 2rem; /* Spacing between the image and the text block */
    flex-wrap: nowrap;
  }
  
  /* Image: Rectangle with light blue border */
  .hero-profile-image img {
    width: 420px; 
    height: 280px; 
    object-fit: cover;
    border-radius: 8px;
    border: 4px solid #3498db; /* Theme light blue */
    box-shadow: 0 6px 16px rgba(0,0,0,0.15);
  }

  /* Text & Buttons block: Centered relative to the Name */
  .hero-profile-layout .hero-info-wrapper {
    display: flex;
    flex-direction: column;
    align-items: center; /* Centers the name, subtitle, and buttons with each other */
    text-align: center;
    margin: 0;
  }

  /* Keeps the buttons side-by-side and spaced evenly */
  .hero-actions {
    display: flex;
    gap: 1rem;
    justify-content: center;
    margin-top: 0.5rem;
  }

  /* Stack profile section on mobile displays */
  @media (max-width: 600px) {
    .hero-profile-layout {
      flex-direction: column !important;
      gap: 2rem;
    }
  }

  /* ========================================== */
  /* 2. MASTER'S THESIS BANNER STYLES           */
  /* ========================================== */
  
  .thesis-card-featured {
    display: flex;
    flex-direction: row;
    background: #A51C30; /* Official Harvard Crimson */
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 4px 15px rgba(0,0,0,0.15);
    margin-bottom: 3rem; /* Spacing between this and the 3 smaller projects below */
    text-decoration: none;
    color: #ffffff; /* High contrast text overlay color */
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }
  
  .thesis-card-featured:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 25px rgba(165, 28, 48, 0.45); /* Tinted crimson shadow drop */
    color: #ffffff;
  }

  /* Video wrapper: Scaled slightly bigger than half (1.2 over 1 ratio) */
  .thesis-media {
    flex: 1.2; 
    min-height: 350px;
    position: relative;
    background: #000; /* Flat backup backdrop color while loading video content */
  }
  
  /* Forces the HTML5 video element to scale to its window boundaries */
  .thesis-media video {
    width: 100%;
    height: 100%;
    object-fit: cover;
    display: block;
  }

  /* Info block container text properties */
  .thesis-info {
    flex: 1; 
    padding: 2.5rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  /* Custom Harvard Location Styling */
  .thesis-location {
    color:rgb(246, 169, 44); /* Warm gold profile accent color */
    font-weight: 700;
    font-size: 1.2rem;
    margin-bottom: 0.5rem;
    display: flex;
    align-items: center;
    gap: 0.6rem; /* Clean layout margin next to image crest */
    text-transform: uppercase;
    letter-spacing: 1px;
  }

  /* Floating Inline University Logo Dimensions */
  .thesis-uni-logo {
    height: 30px; 
    width: auto;
    display: inline-block;
    vertical-align: middle;
  }

  .thesis-title {
    font-size: 1.8rem;
    margin-top: 0;
    margin-bottom: 1rem;
  }

  .thesis-excerpt {
    font-size: 0.8rem;
    line-height: 1.6;
    margin-bottom: 1.5rem;
    opacity: 0.9;
  }

  /* Tag configuration for keywords layout on top of crimson background */
  .thesis-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
  }
  
  .thesis-tag {
    background: rgba(255, 255, 255, 0.15); /* Semi-transparent white pill shapes */
    color: #ffffff;
    padding: 0.4rem 0.8rem;
    border-radius: 20px;
    font-size: 0.8rem;
    font-weight: 600;
    border: 1px solid rgba(255, 255, 255, 0.25);
  }
  
  /* Mobile responsiveness: Stack elements vertically on middle/small viewports */
  @media (max-width: 900px) {
    .thesis-card-featured {
      flex-direction: column;
    }
    .thesis-media {
      min-height: 250px;
    }
  }
</style>

<!-- ========================================== -->
<!-- 3. HERO / INTRODUCTION DISPLAY WRAPPER     -->
<!-- ========================================== -->
<div class="hero-personal">
  <div class="container">
    <div class="hero-content">
      
      <div class="hero-profile-layout">
        
        <!-- Profile Picture (Left Side) -->
        <div class="hero-profile-image">
          <img src="{{ '/assets/images/profile.jpg' | relative_url }}" alt="Profile Photo">
        </div>

        <!-- Text & Buttons Block (Right Side) -->
        <div class="hero-info-wrapper">
          <div class="hero-text">
              <h1 class="hero-name">{{ site.author | default: "Your Name" }}</h1>
              <p class="hero-title">Robotics & Mechatronics Engineer</p>
          </div>
          
          <div class="hero-actions">
            <a href="{{ '/about/' | relative_url }}" class="btn-secondary">
              About
            </a>
              <a href="mailto:{{ site.email }}" class="btn-secondary">
              Contact
            </a>
          </div>
        </div>

      </div>

    </div>
  </div>
</div>

<!-- ========================================== -->
<!-- 4. PORTFOLIO SHOWCASE GRID SECTION         -->
<!-- ========================================== -->
<div class="projects-showcase">
  <div class="container">
    <div class="section-header">
      <h2>Portfolio</h2>
      <p class="section-subtitle">A curated collection of my research and design</p>
    </div>
    
    <!-- === DYNAMIC MASTER'S THESIS BANNER ROW === -->
    {% assign thesis = site.projects | where: "slug", "masters-thesis" | first %}

    <a href="{{ thesis.url | default: '/projects/masters-thesis/' | relative_url }}" class="thesis-card-featured">

      <!-- Left Side: Autoplay Loop Video (Slightly bigger than half width) -->
      <div class="thesis-media">
          <video autoplay loop muted playsinline preload="auto" poster="{{ '/assets/images/projects/thesis/featured.jpg' | relative_url }}">
            <source src="{{ '/assets/images/projects/thesis/demo.mp4' | relative_url }}" type="video/mp4">
            Your browser does not support the video tag.
          </video>
      </div>

      <!-- Right Side: Text & Info Description Details -->
      <div class="thesis-info">
        
        <!-- Location Flag with Custom PNG Crest Logo -->
        <div class="thesis-location">
          <img src="{{ '/assets/images/projects/thesis/harvard-logo.png' | relative_url }}" alt="Harvard Crest" class="thesis-uni-logo"> 
          Harvard University
        </div>
        
        <!-- Title -->
        <h3 class="thesis-title" style="color: #ffffff; font-weight: 700;">
          {{ thesis.title | default: "Your Master's Thesis Title Here" }}
        </h3>
        
        <!-- Brief Description -->
        <p class="thesis-excerpt" style="color: rgba(255, 255, 255, 0.9);">
          {{ thesis.description | default: "A concise description of your research. Explain the core problem, your mechatronic approach, and the impact of the work conducted." }}
        </p>
        
        <!-- Keywords / Tags -->
        <div class="thesis-tags">
          {% if thesis.categories %}
            {% for category in thesis.categories %}
              <span class="thesis-tag">{{ category }}</span>
            {% endfor %}
          {% else %}
            <span class="thesis-tag">Robotics</span>
            <span class="thesis-tag">Control Systems</span>
            <span class="thesis-tag">Kinematics</span>
          {% endif %}
        </div>
          
      </div>
    </a>
    <!-- === END OF MASTER'S THESIS BANNER ROW === -->

    <!-- STANDARD 3-PROJECT ARCHIVE FEATURED GRID -->
    <div class="projects-grid-featured">
    {% assign featured_projects = site.projects | where: "featured", true | sort: "date" | reverse %}
    {% assign all_projects = site.projects | sort: "date" | reverse %}
    {% assign combined_projects = featured_projects | concat: all_projects %}
    {% assign unique_projects = combined_projects | uniq %}
    {% for project in unique_projects limit: 9 %}
      <div class="project-card-featured">
        <div class="project-media">
          {% if project.featured_image %}
            <img src="{{ project.featured_image | relative_url }}" alt="{{ project.title }}" class="project-image">
          {% elsif project.models.first %}
            <div class="model-preview-small">
              <model-viewer 
                src="{{ project.models.first.file | relative_url }}"
                alt="{{ project.title }}"
                camera-controls
                auto-rotate
                class="preview-model-small">
              </model-viewer>
            </div>
          {% else %}
            <div class="project-placeholder-small">
              <i class="fas fa-robot"></i>
            </div>
          {% endif %}
          
          <div class="project-overlay">
            <a href="{{ project.url | relative_url }}" class="project-link-overlay">
              <i class="fas fa-arrow-right"></i>
            </a>
          </div>
        </div>
        
        <div class="project-info-featured">
          <div class="project-categories-small">
            {% for category in project.categories limit:2 %}
              <span class="category-tag-small">{{ category }}</span>
            {% endfor %}
          </div>
          
          <h3 class="project-title-featured">
            <a href="{{ project.url | relative_url }}">{{ project.title }}</a>
          </h3>
          
          <p class="project-excerpt-small">{{ project.description | truncate: 80 }}</p>
          
          <div class="project-features-small">
            {% if project.models %}
              <span class="feature-badge-small" title="3D Models">
                <i class="fas fa-cube"></i>
                {{ project.models.size }}
              </span>
            {% endif %}
            
            {% if project.schematics %}
              <span class="feature-badge-small" title="Schematics">
                <i class="fas fa-microchip"></i>
                {{ project.schematics.size }}
              </span>
            {% endif %}
            
            {% if project.code_files %}
              <span class="feature-badge-small" title="Code Files">
                <i class="fas fa-code"></i>
                {{ project.code_files.size }}
              </span>
            {% endif %}
          </div>
        </div>
      </div>
    {% endfor %}
    </div>

    <div class="showcase-actions">
      <a href="{{ '/projects/' | relative_url }}" class="btn-primary-large">
        <i class="fas fa-th"></i>
        View All Projects
      </a>
    </div>
  </div>
</div>

<!-- ========================================== -->
<!-- 5. TECHNICAL EXPERTISE / SKILLS DISPLAY    -->
<!-- ========================================== -->
<div class="skills-section">
  <div class="container">
    <div class="skills-content">
      <h2>Technical Expertise</h2>
      <div class="skills-grid">
        <div class="skill-category">
          <h3><i class="fas fa-robot"></i> Robotics</h3>
          <div class="skill-tags">
            <span class="skill-tag">ROS</span>
            <span class="skill-tag">Kinematics</span>
            <span class="skill-tag">Path Planning</span>
            <span class="skill-tag">SLAM</span>
          </div>
        </div>
        <div class="skill-category">
          <h3><i class="fas fa-microchip"></i> Electronics</h3>
          <div class="skill-tags">
            <span class="skill-tag">Arduino</span>
            <span class="skill-tag">ESP32</span>
            <span class="skill-tag">PCB Design</span>
            <span class="skill-tag">Sensors</span>
          </div>
        </div>
        <div class="skill-category">
          <h3><i class="fas fa-code"></i> Programming</h3>
          <div class="skill-tags">
            <span class="skill-tag">Python</span>
            <span class="skill-tag">C/C++</span>
            <span class="skill-tag">MATLAB</span>
            <span class="skill-tag">JavaScript</span>
          </div>
        </div>
        <div class="skill-category">
          <h3><i class="fas fa-cube"></i> CAD/Design</h3>
          <div class="skill-tags">
            <span class="skill-tag">SolidWorks</span>
            <span class="skill-tag">Fusion 360</span>
            <span class="skill-tag">3D Printing</span>
            <span class="skill-tag">KiCad</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>