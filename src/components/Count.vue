<script setup>
import { useCounterStore } from '../stores/counter'
import { computed } from 'vue'

const counterStore = useCounterStore()
const count = computed(() => counterStore.count)
const isNegative = computed(() => count.value < 0)
</script>
<template>
  <div class="card__count-wrapper">
    <transition name="fade" mode="out-in">
      <p
        class="card__count"
        :class="isNegative && 'card__count-negative'"
        :key="count">
        {{ count }}
      </p>
    </transition>
  </div>
</template>
<style scoped>
.card__count {
  font-size: 3rem;
  font-weight: bold;
  color: #0196a7;
}

.card__count-wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 4rem;
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
