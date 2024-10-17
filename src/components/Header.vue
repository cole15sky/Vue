<template>
    <header class="flex justify-between items-center p-4 bg-gray-100 dark:bg-gray-900">
      <!-- Logo -->
      <div class="text-2xl font-bold">
        <a href="/">MyWebsite</a>
      </div>
  
      <!-- Navigation Links -->
      <nav>
        <ul class="hidden md:flex space-x-4">
          <li v-for="link in links" :key="link.name">
            <a :href="link.path" class="text-gray-700 dark:text-white hover:text-blue-500">
              {{ link.name }}
            </a>
          </li>
        </ul>
      </nav>
  
      <!-- Theme Switcher Button -->
      <button @click="toggleTheme" class="ml-4 text-sm px-4 py-2 rounded bg-blue-500 text-white hover:bg-blue-700">
        {{ darkMode ? 'Light Mode' : 'Dark Mode' }}
      </button>
  
      <!-- Mobile Menu Toggle -->
      <button @click="toggleMenu" class="md:hidden text-gray-700 dark:text-white">
        <span v-if="isMenuOpen">✖</span>
        <span v-else>☰</span>
      </button>
  
      <!-- Mobile Menu -->
      <div v-if="isMenuOpen" class="absolute top-16 left-0 w-full bg-gray-100 dark:bg-gray-900 md:hidden">
        <ul class="space-y-2 p-4">
          <li v-for="link in links" :key="link.name">
            <a :href="link.path" class="block text-gray-700 dark:text-white hover:text-blue-500">
              {{ link.name }}
            </a>
          </li>
        </ul>
      </div>
    </header>
  </template>
  
  <script>
  export default {
    name: "Header",
    data() {
      return {
        isMenuOpen: false,  // For mobile menu toggle
        darkMode: false,    // Theme toggle (light/dark)
        links: [
          { name: 'Home', path: '/' },
          { name: 'Shop', path: '/shop' },
          { name: 'About', path: '/about' },
          { name: 'Contact', path: '/contact' }
        ]
      };
    },
    methods: {
      toggleMenu() {
        this.isMenuOpen = !this.isMenuOpen;
      },
      toggleTheme() {
        this.darkMode = !this.darkMode;
        document.documentElement.classList.toggle('dark', this.darkMode); // Adds dark class to the root for dark mode
      }
    }
  }
  </script>
  
  <style>
  /* Optionally, you can add some additional styles here */
  </style>
  