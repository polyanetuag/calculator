<template>
  <div id="app">
    <h1>Calculator</h1>
    <Calculator />
  </div>
</template>

<script>
import Calculator from "./main/Calculator.vue"

export default {
  components: { Calculator }
}
</script>

<style>
  @font-face {
    font-family: "RobotoMono";
    src: url("./fonts/RobotoMono-Thin.ttf");
  }

  * {
    font-family: "RobotoMono", monospace;  
  }

  body {
    margin: 0;
  }

  #app {
    display: flex;
    flex-direction: column;
    height: 100vh;
    justify-content: center;
    align-items: center;
    text-align: center;
    color: white;
    background: linear-gradient(to right, #0f0c29, #302b63, #24243e);
  }
</style>