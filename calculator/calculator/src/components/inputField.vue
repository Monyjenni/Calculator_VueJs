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
    }
}
</script>

<style>
.body-col {
    padding-top: 20px;
    display: flex;
    justify-content: center;
    justify-content: space-between;
    margin: 10px 10px 10px 10px;
   
  }</style>