<script setup>
import Counter from './components/Counter.vue'
import Display from './components/Display.vue'
</script>

<template>
  <header>
    <h1>Vue Basic Counter with Shared State</h1>
  </header>

  <main>
    <Counter />
    <Display />
  </main>
</template>

<style scoped>
  header {
    display: flex;
    justify-content: center;
    margin-bottom: 3rem;
  }
</style>
