<template>
  <div id="app">
<h1>Calculator</h1>

<div class="num-input">
  <ul> 
  <li><input type="number" id="myInput1"></li> 
  <button @click="getValue()">Enter</button> 
  <li><input type="number" id="myInput2"></li> 
  <button @click="getValue()">Enter</button>

  </ul>
</div>
<div class="button">
<button @click="onOperatorClick('+')">+</button>
<button @click="onOperatorClick('-')">-</button>
<button @click="onOperatorClick('*')">*</button>
<button @click="onOperatorClick('/')">/</button>
</div>
<div class="result">
  
</div>
  </div>
</template>

<script>

export default {
  name: 'App',
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
