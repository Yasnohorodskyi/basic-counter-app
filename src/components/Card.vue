<script setup>
import Count from "./Count.vue";

defineProps({
  title: {
    type: String,
    default: "",
  },
  subtitle: {
    type: String,
    default: "",
  },
});
</script>

<template>
  <div class="card">
    <h2 class="card__title">{{ title }}</h2>
    <div class="card__subtitle-wrapper">
      <p class="card__subtitle">
        {{ subtitle }}
      </p>
      <Count />
    </div>
    <slot />
  </div>
</template>

<style scoped>
.card {
  background: #fff;
  border-radius: 0.5rem;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
  padding: 1rem 2rem;
  display: flex;
  flex-direction: column;
  max-width: 40rem;
  align-items: center;
  margin: 0 auto;
}

.card__title {
  font-size: 1.5rem;
  margin: 0;
}

.card__subtitle-wrapper {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 1rem;
}

.card__subtitle {
  font-size: 1.25rem;
  margin: 0;
}
</style>
