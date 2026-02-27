<template>
  <div class="glass-container">
    <div
      v-for="card in cards"
      :key="card.id"
      class="glass-card"
      @mouseenter="card.isHovered = true"
      @mouseleave="card.isHovered = false"
      :class="{ 'card-hover': card.isHovered }"
    >
      <div class="card-icon">{{ card.icon }}</div>
      <h3 class="card-title">{{ card.title }}</h3>
      <p class="card-desc">{{ card.description }}</p>
      <div class="card-meta">
        <span class="stat">{{ card.likes }}</span>
        <span class="stat">{{ card.comments }}</span>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const cards = ref([
  {
    id: 1,
    icon: '⚡',
    title: 'Lightning Fast',
    description: 'Optimized performance with lazy loading',
    likes: '2.4k',
    comments: '142',
    isHovered: false
  },
  {
    id: 2,
    icon: '🎨',
    title: 'Pixel Perfect',
    description: 'Every detail crafted with precision',
    likes: '1.8k',
    comments: '89',
    isHovered: false
  },
  {
    id: 3,
    icon: '🔥',
    title: 'Trend Setter',
    description: 'Latest design trends implemented',
    likes: '3.1k',
    comments: '256',
    isHovered: false
  }
])
</script>

<style scoped>
.glass-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 2rem;
  padding: 3rem;
  min-height: 100vh;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  font-family: 'Inter', system-ui, sans-serif;
}

.glass-card {
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(20px);
  border-radius: 24px;
  border: 1px solid rgba(255, 255, 255, 0.2);
  padding: 2rem;
  transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
  cursor: pointer;
}

.glass-card:hover,
.card-hover {
  transform: translateY(-10px) scale(1.02);
  background: rgba(255, 255, 255, 0.15);
  box-shadow: 0 20px 60px rgba(0, 0, 0, 0.2);
  border-color: rgba(255, 255, 255, 0.3);
}

.card-icon {
  font-size: 3rem;
  margin-bottom: 1rem;
  filter: drop-shadow(0 4px 8px rgba(0, 0, 0, 0.2));
}

.card-title {
  color: #ffffff;
  font-size: 1.5rem;
  font-weight: 700;
  margin-bottom: 0.75rem;
  letter-spacing: -0.02em;
}

.card-desc {
  color: rgba(255, 255, 255, 0.85);
  line-height: 1.6;
  margin-bottom: 1.5rem;
  font-size: 0.95rem;
}

.card-meta {
  display: flex;
  gap: 1.5rem;
  padding-top: 1rem;
  border-top: 1px solid rgba(255, 255, 255, 0.1);
}

.stat {
  color: rgba(255, 255, 255, 0.7);
  font-size: 0.85rem;
  font-weight: 600;
}

.stat::before {
  content: '💜 ';
  font-size: 1rem;
}
</style>
