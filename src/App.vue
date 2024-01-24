<script setup>
import { RouterLink, RouterView } from "vue-router";
import Footer from "@/components/Footer.vue";
</script>

<template>
  <header >
   
    <nav class="bg-gray-500 ">
      <div class="max-w-screen-xl  py-3 mx-auto flex items-center">
        <img src="@/assets/hk_logo.jpeg" alt="Logo" class="h-12 w-auto px-1" />
        <ul
          class="flex flex-row font-medium mt-0 space-x-8 rtl:space-x-reverse text-sm"
        >
          <li>
            <router-link
              to="/"
              class="text-dark-blue-900 dark:text-white hover:text-blue-900"
              >Home</router-link
            >
          </li>
          <li>
            <router-link
              to="/about"
              class="text-dark-blue-900 dark:text-white hover:text-blue-900"
              >About</router-link
            >
          </li>
          <li>
            <router-link
              to="/contact"
              class="text-dark-blue-900 dark:text-white hover:text-blue-900"
              >Contact</router-link
            >
          </li>
          
          <!-- Add more navigation links as needed -->
        </ul>
      </div>
    </nav>
  </header>

  <RouterView />
  <Footer />
</template>
