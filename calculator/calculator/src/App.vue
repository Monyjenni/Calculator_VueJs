
<template>
  <div id="app">
    <div class="calculator">
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css">
    <nav class="navbar navbar-dark bg-dark">
      <span class="navbar-brand mb-0 h1">Calculator</span>
    </nav>
    <inputField/>
    <operatorCal/>

<div class="enter-reset">
  <button class="btn btn-primary" @click="getEnter()">Enter</button>
  <button class="btn btn-danger" @click="getReset()">Reset</button>
</div>

<div class="result">
  <p >The result is : {{ result}}</p>
</div>
</div>
  </div>
</template>

<script>

import inputField from './components/inputField.vue';
import operatorCal from './components/operatorCal.vue';

export default {
  name: 'App',
  components: {
    inputField,
    operatorCal
  },
  data(){
    return {
      data:0,
      result:0,
      message: "Testing"
    };
  },
  methods: {
    getEnter (){
      alert("Successfully calculated!!!!")
    },
    getReset (){
      alert("Successfully deleted!!!!")
    },
    calculateResult (){
      switch(this.onOperatorClick('+')){
        case '+':{
          this.result = Number(this.num1) + Number(this.num2)
        }
      }

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
.enter-reset {
  display: flex;
  justify-content: center;
  padding-top:20px
}

</style>
