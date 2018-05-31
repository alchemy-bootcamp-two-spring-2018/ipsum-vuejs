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
  background-color: rgba(241, 108, 85, 0.769);
}

h1 {
  text-align: center;
  background-color:lemonchiffon;
  margin-bottom: 0px;
  margin-right: 100px;
  margin-left: 100px;
  padding-top: 10px;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}

</style>
