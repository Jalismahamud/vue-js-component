<script setup>
const blogs = [
  {
    id: 1,
    title: 'Getting Started with Vue 3',
    author: 'John Doe',
    date: '2025-12-01',
    excerpt: 'Learn the basics of Vue 3 and start building modern web applications.'
  },
  {
    id: 2,
    title: 'Vue 3 Composition API Deep Dive',
    author: 'Jane Smith',
    date: '2025-12-05',
    excerpt: 'Explore the powerful Composition API in Vue 3 and write cleaner code.'
  },
  {
    id: 3,
    title: 'Building Reusable Components',
    author: 'Mike Johnson',
    date: '2025-12-08',
    excerpt: 'Master the art of creating reusable and maintainable Vue components.'
  },
  {
    id: 4,
    title: 'State Management with Pinia',
    author: 'Sarah Lee',
    date: '2025-12-12',
    excerpt: 'Simplify your state management with Pinia, the modern Vue store.'
  },
  {
    id: 5,
    title: 'Vue Router for Single Page Apps',
    author: 'Tom Brown',
    date: '2025-12-15',
    excerpt: 'Create seamless navigation in your Vue applications with Vue Router.'
  }
];
</script>

<template>
  <div class="blog-container">
    <div class="blog-header">
      <h1>Our Blog</h1>
      <p>Latest articles and tutorials</p>
    </div>

    <div class="blog-grid">
      <article v-for="blog in blogs" :key="blog.id" class="blog-card">
        <div class="blog-meta">
          <span class="author">{{ blog.author }}</span>
          <span class="date">{{ blog.date }}</span>
        </div>
        <h2>{{ blog.title }}</h2>
        <p>{{ blog.excerpt }}</p>
        <a href="#" class="read-more">Read More →</a>
      </article>
    </div>
  </div>
</template>

<style scoped>
.blog-container {
  padding: 2rem;
  max-width: 1000px;
  margin: 0 auto;
}

.blog-header {
  background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
  color: white;
  padding: 3rem 2rem;
  border-radius: 8px;
  margin-bottom: 3rem;
  text-align: center;
}

.blog-header h1 {
  font-size: 2.5rem;
  margin: 0 0 1rem 0;
}

.blog-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 2rem;
}

.blog-card {
  background: white;
  border-radius: 8px;
  padding: 2rem;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  transition: transform 0.2s, box-shadow 0.2s;
  border-top: 4px solid #4facfe;
}

.blog-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
}

.blog-meta {
  display: flex;
  justify-content: space-between;
  margin-bottom: 1rem;
  font-size: 0.9rem;
  color: #888;
}

.author {
  font-weight: 600;
  color: #4facfe;
}

.blog-card h2 {
  margin: 1rem 0;
  color: #333;
  font-size: 1.4rem;
}

.blog-card p {
  color: #666;
  line-height: 1.6;
  margin-bottom: 1.5rem;
}

.read-more {
  color: #4facfe;
  text-decoration: none;
  font-weight: 600;
  transition: color 0.2s;
}

.read-more:hover {
  color: #00f2fe;
}
</style>