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
      </section>
    </main>
  </div>
</template>

<script>
import PokemonList from './components/PokemonList.vue';

export default {
  data() {
    return {
      selected: null
    }

  },
  components: {
    PokemonList,
    
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
  margin-top: 50px;
}


.list {
  float: left;
  float: left;
  overflow-y: auto;
  height: 700px;
  max-width: 30%;
}
</style>
