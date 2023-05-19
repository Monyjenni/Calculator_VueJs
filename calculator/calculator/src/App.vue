<template>
  <div id="app">
    <h1>Calculator</h1>

      <div class="num-input">
    <ul> 
  <li><input type="number" v-model.number="num1"  id="myInput2"></li> 
  <button @click="getValue1()">Enter</button> 
  <li><input type="number" v-model="num2"  id="myInput2"></li> 
  <button @click="getValue2()">Enter</button>

  <span>{{ displayNumber }}</span>

  </ul>
</div>
<div class="button">
<button @click="onOperatorClick('+')">+</button>
<button @click="onOperatorClick('-')">-</button>
<button @click="onOperatorClick('*')">*</button>
<button @click="onOperatorClick('/')">/</button>
</div>
<div class="result">
  <button @click="calculateResult">=</button>
  <input type="number" disabled>
</div>
  </div>
</template>

<script>
// import textfield from './components/textfield.vue';

export default {
  name: 'App',
  components: {
    // textfield
  },
  data(){
    return {
      data:0,
      num1: null,
      num2: null
    }
  },
  computed: {
    displayNumber () {
      return this.num1 + ' + ' + this.num2
    }
  },
  methods: {
    getValue1(){
      var inputVal = document.querySelector("#myInput1","#myInput2").value;
      alert("The input value is: " + inputVal);
      console.log(inputVal);
    },
    getValue2(){
      var inputVal = document.querySelector("#myInput2").value;
      alert("The input value is:" + inputVal);
      console.log(inputVal);
    },
    calculateResult (){
      
      

    }
  }
}
</script>

<style>
#app {

  background-color: white;

}
</style>
