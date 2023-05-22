<template>
    <div class="body-col">
        <div class="num-input-col-1">
        <input type="number" v-model.number="num1"  id="myInput1">
      </div>
      <div class="num-input-col-2">
        <input type="number" v-model.number="num2"  id="myInput2">
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