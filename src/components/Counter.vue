<script setup>
import Card from './Card.vue'
import { useCounterStore } from '../stores/counter'

const counterStore = useCounterStore()
</script>

<template>
  <Card title="Counter Component" subtitle="Count:" class="counter">
    <div class="counter-buttons__wrapper">
      <button class="counter-button" @click="counterStore.increment">
        Increment
      </button>
      <button class="counter-button" @click="counterStore.decrement">
        Decrement
      </button>
    </div>
  </Card>
</template>

<style scoped>
.counter {
  margin-bottom: 2rem;
}

.counter-buttons__wrapper {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
  justify-content: space-between;
  padding: 1rem 0 0 0;
  border-top: 2px solid #0196a7;
  width: 100%;
}

.counter-button {
  all: unset;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  padding: 0.75rem 1.5rem;
  border-radius: 1.25rem;
  font-size: 0.75rem;
  font-weight: 500;
  letter-spacing: 0.03em;
  text-transform: uppercase;
  background-color: #0196a7;
  color: white;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
  transition:
    background-color 0.3s ease,
    box-shadow 0.2s ease,
    transform 0.1s ease;
  cursor: pointer;
}

.counter-button:hover {
  background-color: #017f8c;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.15);
}

.counter-button:active {
  background-color: #016d7a;
  transform: scale(0.98);
}

.counter-button:focus-visible {
  outline: 2px solid #0196a7;
  outline-offset: 2px;
}

.counter-button:last-child {
  background-color: #ff4c4c;
  color: white;
}

.counter-button:last-child:hover {
  background-color: #e63946;
}

.counter-button:last-child:active {
  background-color: #d32f2f;
}
</style>
