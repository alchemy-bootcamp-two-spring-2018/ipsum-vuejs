<template>
  <div id="app">
    <header>
      <h1>Lorem Ipsum Selector</h1>
    </header>
    <main>
    <section class="list">
      <IpsumList
      v-bind:selected="selected"
      v-on:select="updateSelected"
      />
    </section>
    <section class="viewer">
      <IpsumViewer v-bind:importedItem = "selected" />
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
        someHtml: '<strong>Hello</strong>'
      };
    },
  components: {
    IpsumList,
    IpsumViewer
  },
  methods: {
    updateSelected(title) {
    this.selected = title;
    }
  }
};
</script>

<style>
h1 {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  font-size: 2.5em;
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
img {
 max-width: 300px;
 display: block;
 margin: 20px;
}

</style>
