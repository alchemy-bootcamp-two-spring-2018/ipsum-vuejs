<template>
  <div id="app">
    <header>
      <h1>Ipsum finder</h1>
    </header>
    <main>
      <section class="list-section">
        <IpsumList
        v-bind:choice="selected"
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
body {
  background-color: rgb(186, 220, 221);
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}

img {
    width: 100px;
}

.ipsum-list {
  list-style: none;
  cursor: pointer;
}

.ipsum-list:hover {
  background-color: lightgray;
}

.list-section {
  color: navy;
  float: left;
  background-color: aqua;
  width: 20%;
  height: 530px;
  overflow: auto;
  padding: 10px;
  border: 2px solid navy;
}

.ipsum-info {
  color:rgb(11, 66, 11);
  float:right;
  width: 70%;
  height: 500px;
  overflow: auto;
  background-color: chartreuse;
  padding: 25px;
  border: 2px solid darkgreen;
}
</style>
