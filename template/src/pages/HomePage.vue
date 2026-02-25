<script setup>
import { ref } from 'vue'
import LinkCard from '@/components/LinkCard.vue'

const profile = ref({
  name: 'Leslie Guillen',
  slogan: 'Full Stack Developer and Teacher',
  imageURL:
    'https://img.freepik.com/premium-photo/cartoon-girl-with-glasses-brown-hair-generative-ai_1034986-18129.jpg',
})
</script>

<template>
  <main class="flex min-h-screen flex-col items-center px-4 py-8">
    <!-- Profile Header -->
    <div class="mb-8 flex flex-col items-center text-center">
      <div
        class="mb-4 h-24 w-24 overflow-hidden rounded-full border-4 border-pink-950 shadow-lg shadow-pink-500/20 sm:h-32 sm:w-32"
      >
        <img
          :src="profile.imageURL"
          :alt="profile.name"
          class="h-full w-full object-cover"
        />
      </div>
      <h1 class="mb-2 font-display text-2xl font-bold text-white sm:text-3xl">
        {{ profile.name }}
      </h1>
      <p class="max-w-xs text-gray-300 sm:text-lg">{{ profile.slogan }}</p>
    </div>

    <!-- Link List -->
    <div class="max-e-w=md flex w-full flex-col gap-4">
      <LinkCard
        v-for="x of [1, 2, 3]"
        :key="x"
      />
    </div>

    <!-- Navigate to Info-->
    <RouterLink
      to="/info"
      class="mt- hover-text-pink-400 text-pink-400 underline-offset-4 transition-colors duration-300 hover:underline"
      >About me ➡️
    </RouterLink>
  </main>
</template>
