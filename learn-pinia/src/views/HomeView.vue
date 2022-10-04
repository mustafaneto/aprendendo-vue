<template>
  <div class="home">
    <h1>Home</h1>
    <div class="counter">{{ storeCounter.counter }}</div>
    <div>
      <button class="buttons" @click="storeCounter.decrement">-</button>
      <button class="buttons" @click="storeCounter.increment">+</button>
      <h1>The double is: {{storeCounter.doubleCount}}</h1>
    </div>
  </div>
</template>

<script setup>
import { useCounterStore } from "@/stores/counter";

const storeCounter = useCounterStore();
</script>

<style scoped>
.counter {
  font-size: 40px;
}
.buttons {
  margin: 10px;
  width: 60px;
  font-size: 40px;
}
</style>
