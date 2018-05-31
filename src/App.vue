<template>
  <div id="app">
    <header>
      <h1>Lorem Ipsum Viewer</h1>
      
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
          v-bind:ipsum="selected"
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
      selected: null
    };
  },
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

.ipsum-list {
  background: lightgray;
  padding: 1%;
  float: left;
}

.ipsum-viewer {
  object-fit: contain;
  height: 671px;
  overflow: auto;
  padding: 3%;
  border: 10px solid lightgray;
}
</style>

