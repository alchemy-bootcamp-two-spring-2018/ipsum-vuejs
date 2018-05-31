<template>
  <div id="app">

    <header>
      <h1>Ipsum Viewer</h1>
    </header>
    
    <section id="list">
      <IpsumList
        v-bind:chosenIpsum="selected"
        v-on:select="updateSelected"
      />
    </section>

    <section id="viewer">
      <IpsumViewer v-bind:ipsum="selected"/>
    </section>

  </div>
</template>

<script>
import IpsumList from './components/IpsumList.vue'
import IpsumViewer from './components/IpsumViewer.vue'

export default {
  data() {
    return {
      selected: null
    }
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
  font-family: 'Roboto Slab', serif;

  
  background: #51DBFF;
  border: 0px;
  display: grid;
  grid-template: 200px 603px / 200px auto;
  grid-template-areas:
    "header viewer"
    "list viewer"
}

header {
  grid-area: header;
  font-family: 'Nixie One', cursive;
  text-align: center;
  padding-top: 30px;
  border-bottom: 2px solid white;
}

#list {
  grid-area: list;
}

#viewer {
  grid-area: viewer;
  border-left: 2px solid white;
  padding: 30px;
  overflow: scroll;
}

h1 {
  margin: 0px;
  font-size: 3em;
}
/* why did the following selectors not work being placed in IpsumViewer.vue? */
img {
  max-width: 250px;
}

.pull-right {
  float: right;
  margin: 10px 0px 10px 10px;
}

.pull-left {
  float: left;
  margin: 10px 10px 10px 0px;
}
</style>
