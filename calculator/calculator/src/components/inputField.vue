<template>
    <div id="#app">
        <div class="body-col">
            
            <div class="num-input-col-1">
            <input type="number" v-model.number="num1"  id="myInput1" placeholder="Your input 1" >
          </div>
          <div class="num-input-col-2">
            <input type="number" v-model.number="num2"  id="myInput2" placeholder="Your input 2" >
          </div>
          </div>
        <div class="display-number">
            <span>Your Input: {{ displayNumber }}</span>
        </div>
        <div class="enter-reset">
            <div class="button-1"><button class="btn btn-primary" @click.prevent="getEnter()" >Enter</button></div>
            <div class="button-2"><button class="btn btn-danger" @click.prevent="getReset()" >Reset</button></div>
            
          </div>
    </div>
    
      
      
</template>

<script>
export default {
    name: 'inputField',
    data () {
        return {
            num1: 0,
            num2: 0,
            
        }
    },
    computed :{
        displayNumber(){
            return this.num1 + ' ' + '+' + ' ' + this.num2
        }
    },
    getEnter (){
      alert("Successfully calculated!!!!")
    },
    getReset (){
      alert("Successfully deleted!!!!")
      this.myInput1 = 0
      this.myInput2= 0
      
      
    },
}
</script>

<style>
.body-col {
    padding-top: 20px;
    display: flex;
    justify-content: center;
    justify-content: space-between;
    margin: 10px 10px 10px 10px;
   
  }
  .enter-reset {
    display: flex;
    justify-content: center;
    padding-top:20px
  }
  .button-1 {
    margin-right: 20px;
  }
</style>