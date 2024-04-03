<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <Stock6Sign msg="Welcome to TEST TEST TEST!"/>
</template>

<script>
import Stock6Sign from './components/Stock6Sign.vue'

export default {
  name: 'App',
  components: {
    Stock6Sign
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
