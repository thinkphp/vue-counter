<script>
  export default {
    data: () => ({
      counter: 0
    }),
    methods: {
      increment() {
        this.counter++;
      },
      decrement() {
        this.counter--;
      },
      reset() {
        this.counter = 0;
      }
    },
    computed: {
      counterColor() {
        if (this.counter > 0) return 'green';
        if (this.counter < 0) return 'red';
        return 'black';
      }
    }
  }
</script>

<template>
  <div class="container">
    <img src="./assets/logo.svg" alt="Vue logo" width="125" height="125">
    <small><h1>Hello World from Vue.js 3!</h1></small>
    <hr>
    <h2 :style="{ color: counterColor }">Counter: {{ counter }}</h2>
    <div class="buttons">
      <button @click="increment()">+1</button>
      <button @click="decrement()">-1</button>
      <button @click="reset()">Reset</button>
    </div>
  </div>
</template>

<style scoped>
.container {
  text-align: center;
  background-color: #f7f7f7;
  padding: 50px;
  border-radius: 10px;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
}

small {
  color: #888;
}

h1 {
  font-weight: bolder;
  color: #333;
}

h2 {
  font-size: 2.5rem;
  margin-top: 20px;
}

.buttons {
  display: flex;
  justify-content: center;
  gap: 15px;
  margin-top: 30px;
}

button {
  cursor: pointer;
  font-size: 1.5rem;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  background-color: #007bff;
  color: white;
  transition: background-color 0.3s ease, transform 0.2s ease;
}

button:hover {
  background-color: #0056b3;
  transform: scale(1.1);
}

button:active {
  background-color: #003c82;
  transform: scale(1);
}
</style>

