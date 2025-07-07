---
layout: page
title: Get In Touch
description: "Have a question or want to work together? Send me a message and I'll get back to you as soon as possible."
form:
  name: contact
  action: https://formspree.io/f/your-form-id
  fields:
    - name: name
      label: Name
      type: text
      required: true
    - name: email
      label: Email
      type: email
      required: true
    - name: subject
      label: Subject
      type: text
      required: true
    - name: message
      label: Message
      type: textarea
      required: true
  submit: Send Message
  success: /contact/thanks/
---

<div class="contact-container">
  <div class="contact-info">
    <h2>Contact Information</h2>
    <p>Feel free to reach out to me through any of the following channels. I typically respond within 24-48 hours.</p>
    
    <div class="contact-methods">
      <div class="contact-method">
        <div class="contact-icon">
          <i class="fas fa-envelope"></i>
        </div>
        <div class="contact-details">
          <h3>Email</h3>
          <a href="mailto:me@mohsinqureshi.ca">me@mohsinqureshi.ca</a>
        </div>
      </div>
      
      <div class="contact-method">
        <div class="contact-icon">
          <i class="fab fa-linkedin"></i>
        </div>
        <div class="contact-details">
          <h3>LinkedIn</h3>
          <a href="https://linkedin.com/in/yourprofile" target="_blank">linkedin.com/in/yourprofile</a>
        </div>
      </div>
      
      <div class="contact-method">
        <div class="contact-icon">
          <i class="fab fa-github"></i>
        </div>
        <div class="contact-details">
          <h3>GitHub</h3>
          <a href="https://github.com/mohsin0803" target="_blank">github.com/mohsin0803</a>
        </div>
      </div>
      
      <div class="contact-method">
        <div class="contact-icon">
          <i class="fab fa-twitter"></i>
        </div>
        <div class="contact-details">
          <h3>Twitter</h3>
          <a href="https://twitter.com/yourusername" target="_blank">@yourusername</a>
        </div>
      </div>
    </div>
    
    <div class="office-hours">
      <h3>Office Hours</h3>
      <p>Monday - Friday: 9:00 AM - 5:00 PM EST</p>
      <p>Weekends: Available by appointment</p>
    </div>
  </div>
  
  <div class="contact-form-container">
    <h2>Send Me a Message</h2>
    <p>Have a question or want to discuss a project? Fill out the form below and I'll get back to you as soon as possible.</p>
    
    <form id="contact-form" action="{{ page.form.action }}" method="POST">
      {% for field in page.form.fields %}
        <div class="form-group">
          <label for="{{ field.name }}">
            {{ field.label }}
            {% if field.required %}<span class="required">*</span>{% endif %}
          </label>
          
          {% if field.type == 'textarea' %}
            <textarea 
              id="{{ field.name }}" 
              name="{{ field.name }}" 
              class="form-control" 
              rows="6"
              {% if field.required %}required{% endif %}></textarea>
          {% else %}
            <input 
              type="{{ field.type }}" 
              id="{{ field.name }}" 
              name="{{ field.name }}" 
              class="form-control"
              {% if field.required %}required{% endif %}>
          {% endif %}
        </div>
      {% endfor %}
      
      <div class="form-actions">
        <button type="submit" class="btn btn-primary">
          <i class="fas fa-paper-plane"></i> {{ page.form.submit }}
        </button>
      </div>
    </form>
    
    <div class="form-note">
      <p><small>By submitting this form, you agree to our <a href="/privacy-policy/">Privacy Policy</a>.</small></p>
    </div>
  </div>
</div>

<div class="faq-section">
  <h2>Frequently Asked Questions</h2>
  
  <div class="faq-item">
    <h3>How soon can I expect a response?</h3>
    <p>I typically respond to all inquiries within 24-48 hours during business days. If you haven't heard back within that time, please check your spam folder or try reaching out through another channel.</p>
  </div>
  
  <div class="faq-item">
    <h3>Do you offer freelance/consulting services?</h3>
    <p>Yes, I'm available for select freelance and consulting projects. Please provide details about your project in your message, and I'll let you know if I can help.</p>
  </div>
  
  <div class="faq-item">
    <h3>Can I schedule a meeting or call?</h3>
    <p>Absolutely! Once you send me a message, I'll respond with my availability to schedule a call or video meeting at a time that works for both of us.</p>
  </div>
  
  <div class="faq-item">
    <h3>Do you speak at conferences or events?</h3>
    <p>I'm always open to speaking opportunities. Please provide details about your event, including the topic, audience, and expected date, and I'll get back to you with my availability.</p>
  </div>
</div>
