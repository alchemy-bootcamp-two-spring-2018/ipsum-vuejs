<template>
  <div id="app">
    <header>
      <h1>Ipsum Viewer</h1>
    </header>
    <main>
      <section class="ipsum-list">
        <IpsumList
          v-bind:selected="selected"
          v-on:select="updateSelected"
        />
      </section>
      <section class="ipsum-viewer">
        <IpsumViewer
          v-bind:ispum="selected"
        />
      </section>
    </main>
  </div>
</template>

<script>
import IpsumList from './components/IpsumList.vue'
import IpsumViewer from './components/IpsumViewer.vue'

export default {
  data() {
    return {
    
    }
  },
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
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

