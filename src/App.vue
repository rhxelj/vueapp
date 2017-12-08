<template>
  <div id="app">
    <img src="./assets/logo.png">
    <Test msg="Passed as properties"></Test>
  </div>

</template>

<script>
import Test from './components/test'

export default {
  name: 'app',
  components: { Test
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
