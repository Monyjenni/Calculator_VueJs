<template>
  <div id="app">
    <nav class="navbar navbar-dark bg-grey">
      <span class="navbar-brand mb-0 h1">Navbar</span>
    </nav>
    <HelloWorld msg="Welcome Mony"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style lang="scss">
@import "~@/assets/scss/vendors/bootstrap-vue/index";
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  
}
</style>
