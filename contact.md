---
layout: default
title: "Contact"
permalink: /contact/
---

<style>
  /* Contact page container styled identically to the project pages */
  .contact-wrapper {
    max-width: 850px;
    margin: 8rem auto 4rem auto;
    padding: 0 2rem;
    font-family: system-ui, -apple-system, sans-serif;
    color: #e0e0e0;
  }

  .contact-title {
    font-size: 2.8rem;
    font-weight: 800;
    margin-bottom: 3.5rem;
    color: #ffffff;
    line-height: 1.2;
  }

  /* Split layout setup: Info details on left, Form interface on right */
  .contact-grid {
    display: grid;
    grid-template-columns: 1fr 1.3fr;
    gap: 4rem;
    align-items: start;
  }

  /* LEFT SIDE: Contact Direct Info Cards */
  .contact-info-column h2, 
  .contact-form-column h2 {
    font-size: 1.5rem;
    font-weight: 700;
    margin-bottom: 2rem;
    color: #ffffff;
    text-transform: uppercase;
    letter-spacing: 0.5px;
    border-bottom: 2px solid #3498db; /* Solid Light Blue Theme Line */
    padding-bottom: 0.5rem;
  }

  .info-detail-block {
    margin-bottom: 2rem;
  }

  .info-label {
    color: #3498db;
    font-weight: 600;
    font-size: 1.1rem;
    display: block;
    margin-bottom: 0.4rem;
  }

  .info-value {
    font-size: 1.05rem;
    color: #cccccc;
    text-decoration: none;
    transition: color 0.2s ease;
  }

  a.info-value:hover {
    color: #3498db;
  }

  /* RIGHT SIDE: Interactive Form Container Styles */
  .contact-form-card {
    background: rgba(30, 35, 45, 0.4);
    border: 2px solid #3498db; /* Premium light blue card border outline */
    border-radius: 15px; /* Matches project 15px curve geometry */
    padding: 2rem;
    box-shadow: 0 10px 30px rgba(52, 152, 219, 0.05);
  }

  .form-group {
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
    margin-bottom: 1.5rem;
  }

  .form-group label {
    font-size: 0.95rem;
    font-weight: 600;
    color: #ffffff;
  }

  .form-group input, 
  .form-group textarea {
    width: 100%;
    padding: 0.75rem 1rem;
    background: rgba(20, 25, 35, 0.8);
    border: 1px solid rgba(52, 152, 219, 0.3);
    border-radius: 8px;
    color: #ffffff;
    font-size: 1rem;
    font-family: inherit;
    transition: border-color 0.2s ease, box-shadow 0.2s ease;
  }

  .form-group input:focus, 
  .form-group textarea:focus {
    outline: none;
    border-color: #3498db;
    box-shadow: 0 0 0 3px rgba(52, 152, 219, 0.2);
  }

  /* Form Submission Action Button Element */
  .btn-submit-form {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    width: 100%;
    padding: 0.85rem 1.5rem;
    background: #3498db;
    color: #ffffff;
    border: none;
    border-radius: 8px;
    font-size: 1rem;
    font-weight: 600;
    cursor: pointer;
    transition: background 0.2s ease, transform 0.1s ease;
  }

  .btn-submit-form:hover {
    background: #2980b9;
  }

  .btn-submit-form:active {
    transform: scale(0.98);
  }

  /* Responsive Transformation for Tablet & Mobile Layout Views */
  @media (max-width: 800px) {
    .contact-grid {
      grid-template-columns: 1fr;
      gap: 3rem;
    }
  }
</style>

<div class="contact-wrapper">
  
  <h1 class="contact-title">Contact</h1>

  <div class="contact-grid">
    
    <!-- LEFT COLUMN: DIRECT CHANNELS -->
    <div class="contact-info-column">
      <h2>Get In Touch</h2>
      
      <div class="info-detail-block">
        <span class="info-label">Email Address</span>
        <a href="mailto:{{ site.email }}" class="info-value">{{ site.email | default: "filippoandrea.mariani@mail.polimi.it" }}</a>
      </div>

      <div class="info-detail-block">
        <span class="info-label">Phone Number</span>
        <a href="tel:+390000000000" class="info-value">+39 3427581838</a> <!-- Edit phone number here -->
      </div>

      <div class="info-detail-block">
        <span class="info-label">Location</span>
        <span class="info-value">Milan, Italy</span>
      </div>
    </div>

    <!-- RIGHT COLUMN: INTERACTIVE EMAIL INBOX FORM -->
    <div class="contact-form-column">
      <h2>Send a Message</h2>
      
      <div class="contact-form-card">
        <!-- Formspree service acts as the secure action hook endpoint pipeline -->
        <form action="https://formspree.io/f/filippoandrea.mariani@mail.polimi.it" method="POST">
          
          <!-- Sender Email -->
          <div class="form-group">
            <label for="email">Your Email Address</label>
            <input type="email" id="email" name="_replyto" placeholder="name@example.com" required>
          </div>

          <!-- Email Object/Subject -->
          <div class="form-group">
            <label for="subject">Object</label>
            <input type="text" id="subject" name="_subject" placeholder="Project collaboration request" required>
          </div>

          <!-- Email Message Content Body text -->
          <div class="form-group">
            <label for="message">Message Text</label>
            <textarea id="message" name="message" rows="6" placeholder="Write your message here..." required></textarea>
          </div>

          <!-- Protection honeypot configuration field against bots spamming -->
          <input type="text" name="_gotcha" style="display:none">

          <!-- Submit Trigger Button -->
          <button type="submit" class="btn-submit-form">Send Message</button>
          
        </form>
      </div>
    </div>

  </div>
</div>