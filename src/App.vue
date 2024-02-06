<script setup>
import Navbar from './components/Navbar.vue'
</script>

<template>
  <div class="wrapper">
    <header class="header">
      <Navbar />
    </header>
    <main>
    </main>
  </div>
</template>

<style scoped>
.header {
  background-color: var(--color-background);
  padding-inline: 46px;
  width: 100vw;

  opacity: 0.8;
}

@media (max-width: 768px) {
  .header {
    height: 100vh;
  }
}
</style>
