<template>
  <div id="app">
    <header>
      <h1>Pokemon Viewer</h1>
    </header>
    <main>
      <section class="list">
        <PokemonList
          v-bind:selected="selected"
          v-on:select="updateSelected"
        />
      </section>
      <section class="viewer">
        <PokemonViewer v-bind:pokemon="selected"/>
      </section>
    </main>
  </div>
</template>

<script>
import PokemonList from './components/PokemonList.vue';
import PokemonViewer from './components/PokemonViewer.vue';

export default {
  data() {
    return {
      selected: null
    }
  },

  components: {
    PokemonList,
    PokemonViewer
  },

  methods: {
    updateSelected(pokemon) {
      this.selected = pokemon;
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

main {
  display: flex;
  justify-content: center;
}

.list {
  min-width: 430px;
}

</style>
