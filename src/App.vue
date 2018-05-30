<template>
  <div id="app">
    <img src="./assets/logo.png">
    <IpsumList msg="Ipsum Viewer"/>
  </div>
</template>

<script>
import IpsumList from './components/IpsumList.vue'

export default {
  name: 'app',
  components: {
    IpsumList
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
