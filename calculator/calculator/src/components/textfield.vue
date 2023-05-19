<template>
    <input :type="text"   id="myInput1"/>
</template>

<script>
export default {
    name: 'TextField',
    props: {
        text: {
            type: Number,
            default: 0
        }
    }
}
</script>