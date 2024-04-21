<template>
  <header>
    <div class="bg-gray-800 mb-2">
      <div class="container mx-auto px-4">
        <nav class="flex items-center justify-between py-4">
          <div class="flex items-center">
            <h1 class="text-white text-lg font-semibold">J A N R I X</h1>
          </div>
          <div class="hidden md:flex items-center justify-center space-x-4 py-4">
            <RouterLink to="/" class="text-white hover:text-gray-300 font-semibold font-sans mr-2">Home</RouterLink>
            <RouterLink to="/about" class="text-white hover:text-gray-300 font-semibold font-sans mr-2">About</RouterLink>
            <RouterLink to="/contact" class="text-white hover:text-gray-300 font-semibold font-sans mr-2">Contact</RouterLink>
            <RouterLink to="/project" class="text-white hover:text-gray-300 font-semibold font-sans mr-2">Projects</RouterLink>
          </div>
          <div class="md:hidden">
            <!-- Mobile Menu Button -->
            <button @click="openMobileMenu = !openMobileMenu" class="text-white focus:outline-none">
              <svg class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path>
              </svg>
            </button>
          </div>
        </nav>
        <!-- Mobile Menu -->
        <div v-if="openMobileMenu" class="md:hidden">
          <div class="flex flex-col space-y-4 text-center py-2 mb-2">
            <RouterLink to="/" class="text-white hover:text-gray-300 font-bold">Home</RouterLink>
            <RouterLink to="/about" class="text-white hover:text-gray-300 font-bold">About</RouterLink>
            <RouterLink to="/contact" class="text-white hover:text-gray-300 font-bold">Contact</RouterLink>
            <RouterLink to="/project" class="text-white hover:text-gray-300 font-bold">Projects</RouterLink>
          </div>
        </div>
      </div>
    </div>
  </header>

  <RouterView />

  <footer class="bg-gray-800 text-white py-20">
    <div class="container mx-auto px-4">
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <!-- Footer Logo -->
        <div class="col-span-1 md:col-span-2">
          <h2 class="text-2xl font-bold">J A N R I X</h2>
          <p class="mt-4">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam convallis dolor et metus ultrices, nec tempor nisi rutrum.</p>
        </div>
        </div>
      <hr class="my-8 border-gray-700 ">
      <p class="text-center">&copy; 2024 My Portfolio. All rights reserved.</p>
    </div>
  </footer>

</template>

<script setup>
import { RouterLink, RouterView } from 'vue-router'

// Reactive data for mobile menu
import { ref } from 'vue'
const openMobileMenu = ref(false)
</script>

<style scoped>
/* No need to include styles here as Tailwind CSS classes are used directly in the template */

/* Active link style */
.router-link-exact-active {
  border-bottom: 2px solid white; /* Add a line below active link */
}
</style>
