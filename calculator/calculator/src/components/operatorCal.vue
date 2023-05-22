<template>
    <div class="operator-calculator">
        <button class="btn btn-warning" @click="add" id="Op1">+</button>
        <button class="btn btn-warning" @click="substract" id="Op2">-</button>
        <button class="btn btn-warning" @click="multiply" id="Op3">*</button>
        <button class="btn btn-warning" @click="divide" id="Op4">/</button>
        </div>
</template>

<script>
    export default {
        name: 'operatorCalculator'
    }
</script>

<style scoped>

</style>