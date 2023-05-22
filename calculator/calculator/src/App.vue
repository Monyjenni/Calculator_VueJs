
<template>
  <div id="app">
    <div class="calculator">
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css">
    <nav class="navbar navbar-dark bg-dark">
      <span class="navbar-brand mb-0 h1">Calculator</span>
    </nav>
    <inputField/>
    <div class="operator-calculator">
      <button class="btn btn-warning" @click="add" id="Op1">+</button>
      <button class="btn btn-warning" @click="substract" id="Op2">-</button>
      <button class="btn btn-warning" @click="multiply" id="Op3">*</button>
      <button class="btn btn-warning" @click="divide" id="Op4">/</button>
  </div>

<!-- <div class="enter-reset">
  <div class="button-1"><button class="btn btn-primary" @click="getEnter()" >Enter</button></div>
  <div class="button-2"><button class="btn btn-danger" @click="getReset()" id="clear">Reset</button></div>
  
</div> -->

<div class="result">
  <p >The result is : {{ result}}</p>
</div>
</div>
  </div>
</template>

<script>

import inputField from './components/inputField.vue';


export default {
  name: 'App',
  components: {
    inputField,
  },
  data(){
    return {
      data:0,
      result:0,
      message: "Testing",
      clear:false
    };
  },
  methods: {
    
    calculateResult (){
      switch(this.onOperatorClick('+')){
        case '+':{
          this.result = Number(this.num1) + Number(this.num2)
        }
      }

    } ,
    add() {
      alert('hi dear! ')
    }

    }
  }
</script>

<style>

#app {
  
background-color:aquamarine;

}
.num-input-col-2 {
  display: flex;
  align-items:center ;
}

.calculator {
  border: 1px solid #ccc;
  border-radius: 10px;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 500px;
  height: 500px;
}

.operator-calculator {
  justify-content: center;
  display: flex;
  padding-top: 20px;
  
}




</style>
