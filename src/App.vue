<template>
  <div id="app">
    <header>
      <h1>Ipsum Viewer</h1>
      <p v-html="someHtml"></p>
    </header>
    <main>
      <section class="list">
        <IpsumList 
          v-bind:selected="selected"
          v-on:select="updateSelected"
        />
      </section>
      <section class="viewer">
        <IpsumViewer v-bind:impsum="selected"/>
      </section>
    </main>
  </div>
</template>

<script>
import IpsumList from './components/IpsumList.vue';
import IpsumViewer from './components/IpsumViewer.vue';

export default {
  data() {
    return {
      selected: null,
      someHtml: '<strong>Hello Ipsum fan!</strong>'
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
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale; 
  color: #2c3e50;
  margin-top: 60px;
}

.list {
  float: left;
  max-width: 500px;
  background: lightsteelblue;
}

.viewer {
  display: inline-block;
}

</style>