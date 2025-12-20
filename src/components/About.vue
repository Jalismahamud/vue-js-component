<script setup>

</script>

<template>
  <div class="about-container">
    <div class="about-header">
      <h1>About Us</h1>
      <p>Learn more about our mission and team</p>
    </div>

    <section class="about-content">
      <div class="about-text">
        <h2>Our Mission</h2>
        <p>We are dedicated to providing the best web development solutions using modern technologies like Vue 3. Our team consists of experienced developers passionate about creating exceptional user experiences.</p>
      </div>

      <div class="about-text">
        <h2>Our Values</h2>
        <ul>
          <li>Innovation and continuous improvement</li>
          <li>Quality and excellence</li>
          <li>Customer satisfaction</li>
          <li>Transparency and honesty</li>
          <li>Collaboration and teamwork</li>
        </ul>
      </div>

      <div class="about-text">
        <h2>Our Team</h2>
        <p>Our team of talented developers and designers work together to bring your vision to life. With years of experience in web development, we're ready to take on any challenge.</p>
      </div>
    </section>
  </div>
</template>

<style scoped>
.about-container {
  padding: 2rem;
  max-width: 900px;
  margin: 0 auto;
}

.about-header {
  background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
  color: white;
  padding: 3rem 2rem;
  border-radius: 8px;
  margin-bottom: 3rem;
  text-align: center;
}

.about-header h1 {
  font-size: 2.5rem;
  margin: 0 0 1rem 0;
}

.about-content {
  display: flex;
  flex-direction: column;
  gap: 2rem;
}

.about-text {
  background: white;
  padding: 2rem;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  border-left: 4px solid #f5576c;
}

.about-text h2 {
  color: #f5576c;
  margin-top: 0;
}

.about-text p {
  line-height: 1.6;
  color: #555;
}

.about-text ul {
  list-style-position: inside;
  color: #555;
  line-height: 1.8;
}

.about-text li {
  margin-bottom: 0.5rem;
}
</style>