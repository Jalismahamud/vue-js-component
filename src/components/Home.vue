<script setup>

</script>

<template>
  <div class="home-container">
    <header class="hero">
      <h1>Welcome to Our Website</h1>
      <p>Build amazing web applications with Vue 3</p>
      <button class="cta-button">Get Started</button>
    </header>

    <section class="features">
      <h2>Why Choose Us?</h2>
      <div class="feature-grid">
        <div class="feature-card">
          <h3>🚀 Fast</h3>
          <p>Lightning-fast performance for your applications</p>
        </div>
        <div class="feature-card">
          <h3>🎨 Beautiful</h3>
          <p>Create stunning user interfaces with ease</p>
        </div>
        <div class="feature-card">
          <h3>🔧 Easy</h3>
          <p>Simple and intuitive API for developers</p>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>
.home-container {
  padding: 2rem;
}

.hero {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  padding: 4rem 2rem;
  border-radius: 8px;
  text-align: center;
  margin-bottom: 3rem;
}

.hero h1 {
  font-size: 2.5rem;
  margin: 0 0 1rem 0;
}

.hero p {
  font-size: 1.2rem;
  margin-bottom: 2rem;
}

.cta-button {
  background: white;
  color: #667eea;
  padding: 0.8rem 2rem;
  border: none;
  border-radius: 4px;
  font-size: 1rem;
  font-weight: bold;
  cursor: pointer;
  transition: transform 0.2s;
}

.cta-button:hover {
  transform: scale(1.05);
}

.features h2 {
  text-align: center;
  font-size: 2rem;
  margin-bottom: 2rem;
  color: #333;
}

.feature-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
}

.feature-card {
  background: #f5f5f5;
  padding: 2rem;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  transition: transform 0.2s;
}

.feature-card:hover {
  transform: translateY(-5px);
}

.feature-card h3 {
  color: #667eea;
  margin-top: 0;
}
</style>