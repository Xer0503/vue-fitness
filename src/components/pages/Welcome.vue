<script setup>
import { ref, onMounted } from 'vue'
import Fit from '../../assets/fitness.png'

const bgImageStyle = ref({})

onMounted(() => {
  // Check if screen is small (less than md = 768px)
  if (window.innerWidth < 768) {
    bgImageStyle.value = {
      backgroundImage: `url(${Fit})`,
    }
  }
})
</script>

<template>
  <div class="h-screen bg-gray-800">
    <div
      id="welcome"
      class="grid md:grid-cols-2 gap-0 bg-cover bg-center md:bg-gray-700"
      :style="bgImageStyle"
    >
      <!-- Left section -->
      <div class="flex justify-center items-center h-screen p-5 text-center bg-black/60 md:bg-transparent">
        <div class="flex flex-col gap-4">
          <h1 class="text-5xl md:text-6xl font-bold text-white">THE BEST FITNESS STUDIO IN TOWN</h1>
          <p class="text-white text-center">Lorem ipsum dolor sit amet consectetur adipisicing elit...</p>
          <span class="text-center">
            <button class="py-2 px-3 rounded-2xl bg-white w-50 text-center hover:text-white hover:bg-orange-600">
              <a href="#">Build Now</a>
            </button>
          </span>
        </div>
      </div>

      <!-- Right image on md+ -->
      <div class="hidden md:block">
        <img :src="Fit" alt="Company Logo" loading="lazy" class="h-screen mx-auto mb-4" />
      </div>
    </div>
  </div>
</template>

<style scoped>
</style>
