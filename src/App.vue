<template>
  <div id="app">
    <header>
    <h1>Vué.js Pokémon Pokédex</h1>
    </header>
    <main>
      <section class="list">
        <Pokemon-list/>
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
  /* max-width: 30%; */
}
</style>
