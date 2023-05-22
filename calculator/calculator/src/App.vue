
<template>
  <div id="app">
    <div class="calculator">
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css">
    <nav class="navbar navbar-dark bg-dark">
      <span class="navbar-brand mb-0 h1">Calculator</span>
    </nav>
  <div class="body-col">
  <div class="num-input-col-1">
  <input type="number" v-model.number="num1"  id="myInput1">
</div>
<div class="num-input-col-2">
  <input type="number" v-model.number="num2"  id="myInput2">
</div>
</div>
<div class="operator">
<button class="btn btn-warning" @click="add" id="Op1">+</button>
<button class="btn btn-warning" @click="substract" id="Op2">-</button>
<button class="btn btn-warning" @click="multiply" id="Op3">*</button>
<button class="btn btn-warning" @click="divide" id="Op4">/</button>
</div>
<div class="enter-reset">
  <button class="btn btn-primary" @click="getEnter()">Enter</button>
  <button class="btn btn-danger" @click="getReset()">Reset</button>
</div>

<div class="display-number">
  <!-- <p v-if="displayOp">{{ message }}</p> -->
  <span>Your Input: {{ displayNumber }}</span>
</div>
<div class="result">
  <p >The result is : {{ result}}</p>
</div>
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
      result:0,
      num1: 0,
      num2: 0,
      message: "Testing"
    };
    
  },
  computed: {
  displayNumber () {
    return this.num1 + '+' + this.num2
  }
},
  methods: {
    getEnter (){
      alert("Successfully calculated!!!!")
    },
    getReset (){
      alert("Successfully deleted!!!!")
    },
    // getValue1(){
    //   var inputVal = document.querySelector("#myInput1").value;
    //   alert("The input value is: " + inputVal);
    //   console.log(inputVal);
    // },
    // getValue2(){
    //   var inputVal = document.querySelector("#myInput2").value;
    //   alert("The input value is:" + inputVal);
    //   console.log(inputVal);
    // },
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
.body-col {
  padding-top: 20px;
  display: flex;
  justify-content: center;
  justify-content: space-between;
  margin: 10px 10px 10px 10px;
 
}
.operator {
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
