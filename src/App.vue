<template>
  <div id="app">
    <header>
      <h1>Lorem Ipsum Selector</h1>
    </header>
    






  </div>
</template>

<script>
import IpsumList from './components/IpsumList.vue'
import IpsumViewer from './components/IpsumViewer.vue'


export default {
  name: 'app',

  components: {
    IpsumList,
    IpsumViewer
  },
  methods: {
    updateSelected(ipsum) {
      this.selected = ipsum;
    }
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
