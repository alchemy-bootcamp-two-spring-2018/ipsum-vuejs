<template>
  <div id="app">
    <header>
      <h1>Lorem Ipsum Selector</h1>
    </header>
    <main>
<section class = "list">
  <IpsumList
    v-bind:selected = "selected"
    v-on:select= "updateSelected"
    />
    <section class = "viewer">
      <IpsumViewer v-bind:ipsum="selected" />
      </section>
    </main>
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
.list {
    float: left;
  width: 35%;
  background-color: #eee;
  padding-top: 10px;
}
.viewer {
  float: right;
  width: 62%;
  border: 1px solid black;
  min-height: 600px;
  padding: 10px;
}

</style>
