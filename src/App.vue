<template>
  <div id="app">
    <header>
      <h1>Ipsum Options</h1>
    </header>
    <main>
      <section class="list">
        <IpsumList 
          v-bind:selected="selected"
          v-on:select="updateSelected"
        />
      </section>
      <section class="viewer">
        <IpsumViewer v-bind:ipsumItem="selected"/>
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
    }
  },
  components: {
    IpsumList,
    IpsumViewer
  },
  methods: {
    updateSelected(ipsumItem) {
      this.selected = ipsumItem;
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
}

.list {
  float: left;
  max-width: 300px;
  background: lavender;
  overflow-y: auto;
}

.viewer {
  height: 80%;
  overflow: auto;
  margin: 10px;
  padding: 10px;
}
</style>
