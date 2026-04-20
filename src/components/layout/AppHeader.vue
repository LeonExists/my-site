<script setup>
import { RouterLink } from 'vue-router'
</script>

<template>
  <header class="app-header">
    <nav class="nav">
      <RouterLink to="/" class="nav-link">Home</RouterLink>
      <RouterLink to="/about" class="nav-link">About</RouterLink>
    </nav>
  </header>
</template>

<style scoped>
.app-header {
  padding: 1rem 2rem;
  border-bottom: 1px solid var(--color-border);
}

.nav {
  display: flex;
  gap: 1.5rem;
}

.nav-link {
  font-weight: 500;
}

.nav-link.router-link-active {
  color: var(--color-heading);
  font-weight: 700;
}
</style>
