<template>
  <footer class="app-footer">
    <p>&copy; {{ new Date().getFullYear() }}</p>
  </footer>
</template>

<style scoped>
.app-footer {
  padding: 1rem 2rem;
  border-top: 1px solid var(--color-border);
  text-align: center;
  font-size: 0.875rem;
  color: var(--color-text);
  opacity: 0.6;
}
</style>
