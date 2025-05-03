<script setup>
import { useCounterStore } from '../stores/counter'
import { computed } from 'vue'

const counterStore = useCounterStore()
const count = computed(() => counterStore.count)
const isNegative = computed(() => count.value < 0)
</script>
<template>
  <transition name="fade" mode="out-in">
    <span
      class="card__count"
      :class="isNegative && 'card__count-negative'"
      :key="count">
      {{ count }}
    </span>
  </transition>
</template>
<style scoped>
.card__count {
  font-size: 3rem;
  font-weight: bold;
  color: #0196a7;
  margin-left: 1rem;
}
.card__count-negative {
  color: #ff4c4c;
}

.fade-leave-active {
  transition:
    opacity 0.3s ease,
    transform 0.3s ease;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
  transform: translateY(-10px);
}
</style>
