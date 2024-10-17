<template>
  <div>
    <h1>Counter: {{ count }}</h1>
    <button @click="increment">Increment</button>
    <button @click="reset">Reset</button>
    <h1> {{ name }}</h1>
  </div>
</template>

<script>
import { ref } from 'vue';

export default {
  setup() {
    // Create a reactive ref for the counter
    const count = ref(0);

    // Function to increment the counter
    const increment = () => {
      count.value++;
    };

    // Function to reset the counter
    const reset = () => {
      count.value = 0;
    };
    const name = ref("ahmet")

    // Return the refs and functions to the template
    return {
      count,
      increment,
      reset,
      name,
    };
  },
};
</script>

<style>
/* Add your styles here */
</style>
