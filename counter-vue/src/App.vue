<script setup>
import { ref } from "vue";

const count = ref(0);

function increase() {
  count.value++;
}

function decrease() {
  count.value--;
}
</script>

<template>
  <main>
    <h1>Counter</h1>
    <span id="value">{{ count }}</span>
    <div>
      <button @click="decrease" id="decrease">-</button>
      <button @click="increase" id="increase">+</button>
    </div>
  </main>
</template>

<style scoped>
main {
  text-align: center;
  background-color: #333333;
  padding: 20px;
  border-radius: 8px;
}

#value {
  font-size: 50px;
}

button {
  font-size: 10px;
  margin: 0 5px;
  background-color: #555555;
  color: #ffffff;
  border: none;
  padding: 10px 20px;
  cursor: pointer;
  border-radius: 4px;
}

button:hover {
  background-color: #777777;
}

button:active {
  animation: pulse 0.5s linear;
}

@keyframes pulse {
  0% {
    transform: scale(1);
  }

  50% {
    transform: scale(1.1);
  }

  100% {
    transform: scale(1);
  }
}
</style>
