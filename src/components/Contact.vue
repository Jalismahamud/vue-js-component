<script setup>
import { ref } from 'vue';

const formData = ref({
  name: '',
  email: '',
  subject: '',
  message: ''
});

const submitted = ref(false);

const handleSubmit = () => {
  if (formData.value.name && formData.value.email && formData.value.message) {
    submitted.value = true;
    setTimeout(() => {
      submitted.value = false;
      formData.value = { name: '', email: '', subject: '', message: '' };
    }, 3000);
  }
};
</script>

<template>
  <div class="contact-container">
    <div class="contact-header">
      <h1>Contact Us</h1>
      <p>We'd love to hear from you. Get in touch with us today!</p>
    </div>

    <div class="contact-content">
      <div class="contact-info">
        <h2>Get in Touch</h2>
        <div class="info-item">
          <h3>📍 Address</h3>
          <p>123 Web Street, Tech City, TC 12345</p>
        </div>
        <div class="info-item">
          <h3>📧 Email</h3>
          <p>info@company.com</p>
        </div>
        <div class="info-item">
          <h3>📞 Phone</h3>
          <p>+1 (555) 123-4567</p>
        </div>
        <div class="info-item">
          <h3>⏰ Hours</h3>
          <p>Monday - Friday: 9:00 AM - 6:00 PM</p>
        </div>
      </div>

      <form @submit.prevent="handleSubmit" class="contact-form">
        <div v-if="submitted" class="success-message">
          ✓ Thank you! Your message has been sent successfully.
        </div>

        <div class="form-group">
          <label for="name">Name *</label>
          <input
            id="name"
            v-model="formData.name"
            type="text"
            placeholder="Your full name"
            required
          />
        </div>

        <div class="form-group">
          <label for="email">Email *</label>
          <input
            id="email"
            v-model="formData.email"
            type="email"
            placeholder="your@email.com"
            required
          />
        </div>

        <div class="form-group">
          <label for="subject">Subject</label>
          <input
            id="subject"
            v-model="formData.subject"
            type="text"
            placeholder="Message subject"
          />
        </div>

        <div class="form-group">
          <label for="message">Message *</label>
          <textarea
            id="message"
            v-model="formData.message"
            placeholder="Your message here..."
            rows="5"
            required
          ></textarea>
        </div>

        <button type="submit" class="submit-btn">Send Message</button>
      </form>
    </div>
  </div>
</template>

<style scoped>
.contact-container {
  padding: 2rem;
  max-width: 1000px;
  margin: 0 auto;
}

.contact-header {
  background: linear-gradient(135deg, #fa709a 0%, #fee140 100%);
  color: white;
  padding: 3rem 2rem;
  border-radius: 8px;
  margin-bottom: 3rem;
  text-align: center;
}

.contact-header h1 {
  font-size: 2.5rem;
  margin: 0 0 1rem 0;
}

.contact-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 3rem;
}

.contact-info {
  background: white;
  padding: 2rem;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
}

.contact-info h2 {
  color: #fa709a;
  margin-top: 0;
}

.info-item {
  margin-bottom: 2rem;
}

.info-item h3 {
  color: #fa709a;
  margin: 0 0 0.5rem 0;
  font-size: 1rem;
}

.info-item p {
  color: #666;
  margin: 0;
  line-height: 1.6;
}

.contact-form {
  background: white;
  padding: 2rem;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
}

.success-message {
  background: #d4edda;
  color: #155724;
  padding: 1rem;
  border-radius: 4px;
  margin-bottom: 1.5rem;
  font-weight: 600;
}

.form-group {
  margin-bottom: 1.5rem;
  display: flex;
  flex-direction: column;
}

.form-group label {
  margin-bottom: 0.5rem;
  color: #333;
  font-weight: 600;
}

.form-group input,
.form-group textarea {
  padding: 0.75rem;
  border: 1px solid #ddd;
  border-radius: 4px;
  font-size: 1rem;
  font-family: inherit;
  transition: border-color 0.2s;
}

.form-group input:focus,
.form-group textarea:focus {
  outline: none;
  border-color: #fa709a;
  box-shadow: 0 0 0 3px rgba(250, 112, 154, 0.1);
}

.submit-btn {
  background: linear-gradient(135deg, #fa709a 0%, #fee140 100%);
  color: white;
  padding: 0.75rem 2rem;
  border: none;
  border-radius: 4px;
  font-size: 1rem;
  font-weight: 600;
  cursor: pointer;
  transition: transform 0.2s;
}

.submit-btn:hover {
  transform: scale(1.02);
}

@media (max-width: 768px) {
  .contact-content {
    grid-template-columns: 1fr;
  }
}
</style>