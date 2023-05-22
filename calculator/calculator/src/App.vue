
<template>
  <div id="app">
    <div class="calculator">
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css">
    <nav class="navbar navbar-dark bg-dark">
      <span class="navbar-brand mb-0 h1">Calculator</span>
    </nav>
    <inputField/>
    <div class="operator-calculator">
      <!-- string operators are called val which is parameter -->
      <button class="btn btn-warning" @click="handleClick('+')" >+</button>
      <button class="btn btn-warning" @click="handleClick('-')" >-</button>
      <button class="btn btn-warning" @click="handleClick('*')" >*</button>
      <button class="btn btn-warning" @click="handleClick('/')" >/</button>

  </div>

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
    
    };
  },
  methods: {
    
    add() {
      alert('hi dear! ')
    },
    handleClick(val) {
      switch(operator){
        case '+':
        this.result= this.num1 + this.num2
        break 
        case '-' 
      }
    }
  
    },
    props : {
      operator: {
        type: String,
        required: true
      },
    },
  
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
