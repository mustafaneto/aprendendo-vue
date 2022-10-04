<template>
  <div class="about">
    <h1>About</h1>
    <button class="buttons" @click="storeCounter.increment">{{ storeCounter.counter }}</button>
    <br>
    <h3>Type new number: </h3>
    <input type="number" v-model="storeCounter.counter">
  </div>
</template>

<script setup>
import { useCounterStore } from "@/stores/counter";

const storeCounter = useCounterStore();
</script>

<style scoped>

.buttons {
  margin: 10px;
  width: auto;
  font-size: 40px;
}
</style>
