<template>
  <div id="app">
    <div class="counter">
      <h1>Counter: {{ count }}</h1>
      <button @click="increment">Increment</button>
      <button @click="decrement" :disabled="count <= 0">Decrement</button>
      <button @click="reset">Reset</button>
      <p v-if="count === 0" style="color: red;">Counter is at zero!</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      count: 0
    };
  },
  methods: {
    increment() {
      this.count++;
    },
    decrement() {
      if (this.count > 0) {
        this.count--;
      }
    },
    reset() {
      this.count = 0;
    }
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.counter {
  margin-top: 50px;
}

button {
  margin: 5px;
}
</style>
