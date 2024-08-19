<script setup>
import { ref } from "vue";

const showText = ref(false);
</script>

<template>
  <main>
    <Transition name="fade">
      <h1 v-if="showText">hello world</h1>
    </Transition>
    <button @click="showText = !showText">toggle</button>
  </main>
</template>

<style scoped>
.fade-enter-from {
  opacity: 0;
}

.fade-enter-to {
  opacity: 1;
}

.fade-enter-active {
  transition: all 1.5s ease;
}
</style>
