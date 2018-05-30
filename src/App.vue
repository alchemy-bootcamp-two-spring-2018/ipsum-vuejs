<template>
  <div id="app">
    <header>
      <h1>Lorem Ipsum Viewer</h1>
    </header>
    <main>
      <section class="list">
        <IpsumList 
          v-bind:selected="selected"
          v-on:select="updateSelected"
        />
      </section>
      <section class="viewer">
        <IpsumViewer v-bind:ipsum="selected"/>
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
      someHtml: '<strong>hello</strong>'
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
  background: rgb(101, 79, 110);
}

.viewer {
  display: inline-block;
}

</style>