<script setup>
import { ref } from 'vue'
import Bar from '../../assets/Bar.png'
import Bar2 from '../../assets/Bar2.png'
import { selectDisplay } from '../../utils/displayState'
const isOpen = ref(false)
</script>

<template>
  <div class="nav flex justify-between items-center px-5 py-2">
    <!-- Logo -->
    <span class="text-2xl font-bold">
      GYM<span class="text-orange-600">SICK</span>
    </span>

    <!-- Desktop Nav -->
    <div class="hidden md:block">
      <ul class="text-center flex space-x-1 md:space-x-6 text-md">
        <li @click="selectDisplay = 1" class="hover:underline hover:text-orange-600 hover:font-semibold"><a href="#">Home</a></li>
        <li @click="selectDisplay = 2" class="hover:underline hover:text-orange-600 hover:font-semibold"><a href="#">Dashboard</a></li>
        <li @click="selectDisplay = 3" class="hover:underline hover:text-orange-600 hover:font-semibold"><a href="#">Workout</a></li>
        <li class="hover:underline hover:text-orange-600 hover:font-semibold"><a href="#about">About Us</a></li>
        <li class="hover:underline hover:text-orange-600 hover:font-semibold"><a href="#contact">Contact</a></li>
      </ul>
    </div>

    <!-- Desktop Button -->
    <span class="hidden md:block">
      <button class="px-2 py-1 w-35 bg-orange-600 text-white rounded text-sm hover:opacity-85">Start Today</button>
    </span>

    <!-- Mobile Hamburger Icon -->
    <div class="block md:hidden">
        <button @click="isOpen = !isOpen">
            <img
            v-if="!isOpen"
            :src="Bar"
            alt="Open Menu"
            class="mx-auto w-10"
            loading="lazy"
            />
            <img
            v-else
            :src="Bar2"
            alt="Close Menu"
            class="mx-auto w-10"
            loading="lazy"
            />
        </button>
    </div>

  </div>

  <!-- Mobile Menu -->
  <div v-if="isOpen" class="md:hidden px-5 pb-4 text-center">
    <ul class="flex flex-col space-y-2 text-md">
      <li @click="selectDisplay = 1" class="hover:underline hover:text-orange-600 hover:font-semibold active:text-orange-600"><a href="#">Home</a></li>
      <li @click="selectDisplay = 2" class="hover:underline hover:text-orange-600 hover:font-semibold active:text-orange-600"><a href="#">Dashboard</a></li>
      <li @click="selectDisplay = 3" class="hover:underline hover:text-orange-600 hover:font-semibold active:text-orange-600"><a href="#">Workout</a></li>
      <li class="hover:underline hover:text-orange-600 hover:font-semibold active:text-orange-600"><a href="#about">About Us</a></li>
      <li class="hover:underline hover:text-orange-600 hover:font-semibold active:text-orange-600"><a href="#contact">Contact</a></li>
      <li>
        <button class="w-35 mt-2 px-2 py-1 bg-orange-600 text-white rounded text-sm">Start Today</button>
      </li>
    </ul>
  </div>
</template>

<style scoped>
</style>
