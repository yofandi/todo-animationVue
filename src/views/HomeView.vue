<script setup>
import { ref } from "vue";

const showText = ref(false);
</script>

<template>
  <main>
    <div class="container">
      <Transition name="fade">
        <h1 v-if="showText">hello world</h1>
        <h1 v-else>Good Bye</h1>
      </Transition>
      <button @click="showText = !showText">toggle</button>
    </div>
  </main>
</template>

<style scoped>
.container {
  position: relative;
}

h1 {
  position: absolute;
}

button {
  margin-top: 100px;
}

.fade-enter-from {
  opacity: 0;
}

.fade-enter-to {
  opacity: 1;
}

.fade-enter-active {
  transition: all 1.5s ease;
}

.fade-leave-from {
  opacity: 1;
}

.fade-leave-to {
  opacity: 0;
}

.fade-leave-active {
  transition: all 1.5s ease;
}
</style>
