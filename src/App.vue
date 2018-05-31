<template>
  <div id="app">
    <header>
      <h1>Listo' Ipsum</h1>
      
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
import IpsumList from './components/IpsumList.vue'
import IpsumViewer from './components/IpsumViewer.vue'

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
  background-color: #67a8a3;
}

h1 {
  font-size: 50px;
  text-align: center;
  background-color:#fbead1;
  margin-bottom: 0px;
  margin-right: 160px;
  margin-left: 160px;
  padding-top: 10px;
  border-radius: 20px 20px 0px 0px;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}

</style>
