<template>
  <section class="px-5 md:px-0">
    <div class="mx-auto featured-container">
      <h2 class="text-4xl font-bold mb-4 text-center text-white" ref="featuredTitle">Featured Slots</h2>
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8" ref="gameGrid">
        <a v-for="game in featuredGames" 
           :key="game.id" 
           :href="game.buttonLink"
           class="game-card rounded-lg overflow-hidden transform hover:scale-105 transition-transform duration-300 block">
          <img :src="game.image" :alt="game.name" class="w-full object-contain">
          <h3 class="text-xl font-bold mb-2 text-white text-center">{{ game.name }}</h3>
        </a>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const featuredTitle = ref(null)
const gameGrid = ref(null)

const featuredGames = ref([
  {
    id: 1,
    name: 'Fortune Tiger',
    image: '/images/games/1.jpg',
    buttonLink: '#'
  },
  {
    id: 2,
    name: 'Sweet Bonanza',
    image: '/images/games/2.jpg',
    buttonLink: '#'
  },
  {
    id: 3,
    name: 'Gates of Olympus',
    image: '/images/games/3.jpg',
    buttonLink: '#'
  },
  {
    id: 4,
    name: 'Wild West Gold',
    image: '/images/games/4.jpg',
    buttonLink: '#'
  },
  {
    id: 5,
    name: 'Starlight Princess',
    image: '/images/games/5.jpg',
    buttonLink: '#'
  },
  {
    id: 6,
    name: 'Sugar Rush',
    image: '/images/games/6.jpg',
    buttonLink: '#'
  }
])
</script>

<style scoped>
.featured-container {
  max-width: 620px;
}

.game-card {
  background: linear-gradient(45deg, #ff4e9b, #12000a);
  transition: all 0.3s ease;
  box-shadow: 0 4px 12px rgba(251, 217, 93, 0.3);
}

.game-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 4px 12px rgba(251, 217, 93, 0.3);
}
</style>
