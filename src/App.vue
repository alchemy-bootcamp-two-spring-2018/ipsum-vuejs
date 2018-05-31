<template>
  <div id="app">
    
    <header>
      <h1>Pokemon</h1>
    </header>

    <main>
      <section class="list">
        <PokemonList
          v-on:select="updateSelected"
          v-bind:selected="selected"
        />
      </section>
      
      <section class="detail-viewer">
        <PokemonViewer
        v-bind:pokemon="selected"
        />
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
};

</script>

<style>

body {
  margin: 0px;
  background-color: whitesmoke;
}
main {
  display: flex;
  justify-content: space-evenly;
}

h1 {
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 4em;
  color: wheat;
  background-image: url("background.jpg");
  background-size: cover;
  height: 2.5em;
  margin: 0px 0px 10px 0px;

}

</style>
