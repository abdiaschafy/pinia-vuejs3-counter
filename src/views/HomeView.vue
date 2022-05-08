<template>
  <div class="home">
    <h1>Home</h1>
    <Counter />
    <div class="buttons">
      <button @click="storeCounter.decrement">-</button>
      <button @click="storeCounter.increment">+</button>
    </div>
    <hr>
    <div>Ceci est un nombre: {{ storeCounter.oddOrEven }}</div>
    <hr>
    <h3>Modifier le compteur</h3>
    <input type="number" v-model="storeCounter.count">
  </div>
</template>

<script setup>
import Counter from "@/components/Counter.vue"
import { useCounterStore } from "@/stores/counter";

const storeCounter = useCounterStore()
</script>

<style>
.count {
  font-size: 50px;
  margin: 20px;
}
.buttons button {
  font-size: 50px;
  margin: 20px;
}
</style>
