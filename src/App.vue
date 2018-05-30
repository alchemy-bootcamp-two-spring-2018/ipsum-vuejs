<template>
  <div id="app">
    <header>
    <h1>Vué.js Pokémon Pokédex</h1>
    </header>
    <main>
      <section class="list">
        <Pokemon-list
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
  font-family: monospace;
  text-align: center;
  margin-top: 50px;
}
.viewer {
  display: inline-block;
  height: 700px;
}

.list {
  float: left;
  overflow-y: auto;
  height: 700px;
  max-width: 35%;
}
</style>
