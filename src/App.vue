<template>
  <div id="app">
    <InputTexto/>
  </div>
</template>

<script>
import InputTexto from "./components/InputTexto.vue";

export default {
  name: 'App',
  components: {
    InputTexto
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
