<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>
<template>
  <div id="app-container">
    <!-- Persistent Navigation Menu -->
    <nav class="navigation-menu">
      <RouterLink to="/" class="nav-link">Home</RouterLink>
      <RouterLink to="/about" class="nav-link">About</RouterLink>
      <RouterLink to="/contact" class="nav-link">Contact</RouterLink>
    </nav>

    <!-- Dynamic Page Display Placeholder -->
    <main class="page-content">
      <RouterView />
    </main>
  </div>
</template>

<style>
/* Global Base Page Layout Style Settings */
body {
  margin: 0;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  background-color: #f4f7f6; /* Custom background tint */
  color: #333333;
}

#app-container {
  max-width: 800px;
  margin: 40px auto;
  padding: 20px;
}

/* Navigation Bar Flexbox Styling */
.navigation-menu {
  display: flex;
  gap: 20px;
  background-color: #2c3e50; /* Dark slate header bar block */
  padding: 15px 20px;
  border-radius: 8px;
  margin-bottom: 30px;
}

/* RouterLink State Styling overrides */
.nav-link {
  color: #ffffff;
  text-decoration: none;
  font-weight: 600;
  padding: 6px 12px;
  border-radius: 4px;
  transition: background-color 0.2s ease;
}

/* Highlight Hover Interaction Effect */
.nav-link:hover {
  background-color: #41b883; /* Vue Green accent tone */
}

/* Main Component Content Separation Box */
.page-content {
  background-color: #ffffff;
  padding: 30px;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
}

h1 {
  color: #2c3e50;
  margin-top: 0;
}
</style>

