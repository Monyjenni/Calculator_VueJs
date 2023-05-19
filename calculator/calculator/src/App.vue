<template>
  <div id="app">
    <h1>Calculator</h1>

      <div class="num-input">
    <ul> 
  <li><input type="number" v-model.number="num1"  id="myInput1"></li> 
  <button @click="getValue1()">Enter</button> 
  <li><input type="number" v-model="num2"  id="myInput2"></li> 
  <button @click="getValue2()">Enter</button>

  <span>{{ displayNumber }}</span>

  </ul>
</div>
<div class="result">
  <button @click="calculateResult">Enter</button>
  <input type="number" disabled>
</div>
<br>
<div class="operator">
<button @click="onOperatorClick('+')" id="Op1">+</button>
<button @click="onOperatorClick('-')" id="Op2">-</button>
<button @click="onOperatorClick('*')" id="Op3">*</button>
<button @click="onOperatorClick('/')" id="Op4">/</button>
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
      var inputVal = document.querySelector("#myInput1").value;
      alert("The input value is: " + inputVal);
      console.log(inputVal);
    },
    getValue2(){
      var inputVal = document.querySelector("#myInput2").value;
      alert("The input value is:" + inputVal);
      console.log(inputVal);
    },
    onOperatorClick(){
    var inputOp = document.querySelector("#Op1").value;
    alert(inputOp);
    console.log(inputOp);
    },
    calculateResult (){
      switch(this.button){
        case '+': {

        }
        case '-':{

        }
        case '*':{
          
        }
        case '/':{
          
        }

      }
      
      

    }
  }
}
</script>

<style>
#app {

  background-color: white;

}
</style>
