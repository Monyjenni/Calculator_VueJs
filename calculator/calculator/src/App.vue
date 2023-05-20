<template>
  <div id="app">
    <h1>Calculator</h1>

  <div class="num-input-col-1">
  <input type="number" v-model.number="num1"  id="myInput1">
  <button @click="getValue1()">Enter</button> 
</div>
<div class="num-input-col-2">
  <input type="number" v-model.number="num2"  id="myInput2">
  <button @click="getValue2()">Enter</button>
</div>
<br>
<div class="operator">
  <div>
<button v-on:click="onOperatorClick1()" id="Op1">+</button>
<p v-if="displayOp">{{ message }}</p>
</div>
<button v-on:click="onOperatorClick('-')" id="Op2">-</button>
<button v-on:click="onOperatorClick('*')" id="Op3">*</button>
<button v-on:click="onOperatorClick('/')" id="Op4">/</button>
</div>
<div class="display-number">
  <br>
  <span>= {{ displayNumber }}</span>
</div>
<div class="result">
  <p>The result is : {{ result}}</p>

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
    } ,
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

  background-color: white;

}
.num-input-col-2 {
  display: flex;
  align-items:center ;
}
</style>
