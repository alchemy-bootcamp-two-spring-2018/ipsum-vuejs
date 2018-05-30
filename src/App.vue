<template>
  <div id="app">
    <header>
      <h1>Ipsum Viewer</h1>
    </header>
    <main>
      <section class="list">
        <IpsumList></IpsumList>
      </section>
      <section class="viewer">
        <IpsumViewer></IpsumViewer>
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
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
