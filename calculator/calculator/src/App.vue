
<template>
  <div id="app">
    <div class="calculator">
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css">
    <nav class="navbar navbar-dark bg-dark">
      <span class="navbar-brand mb-0 h1">Calculator</span>
    </nav>
  <div class="num-input-col-1">
  <input type="number" v-model.number="num1"  id="myInput1" v-on:input="calculateResult">
</div>
<select v-model="operator">
<button v-on:click="add" id="Op1">+</button>
<button v-on:click="substract" id="Op2">-</button>
<button v-on:click="multiply" id="Op3">*</button>
<button v-on:click="divide" id="Op4">/</button>
</select>
<p v-if="displayOp">{{ message }}</p>
<div class="num-input-col-2">
  <input type="number" v-model.number="num2"  id="myInput2" v-on:input="calculateResult">
  
</div>
<br>
<div class="display-number">
  <br>
  <span>= {{ displayNumber }}</span>
</div>
<div class="result">
  <button @click="getResult()">Enter</button>
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
      displayOp: false,
      message: "Testing"
    };
    
  },
  computed: {
    displayNumber () {
      return this.num1 + '+' + this.num2
    }
  },
  methods: {
    getResult (){
      alert("Successfully calculated!!!!")
    },
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
    calculateResult (){
      switch(this.onOperatorClick('+')){
        case '+':{
          this.result = Number(this.num1) + Number(this.num2)
        }
      }

    } ,
    onOperatorClick1(){
      this.displayOp= true;
    } 
    }
  }
</script>



<style>

#app {
  

background-color: rgba(255, 249, 249, 0.866);

}
.num-input-col-2 {
  display: flex;
  align-items:center ;
}
.result {
  padding-top: 50px
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
</style>
