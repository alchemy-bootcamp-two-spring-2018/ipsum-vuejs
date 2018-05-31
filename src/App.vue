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
 
h1 {
    font-size: 5em;
    color: rgb(255, 247, 0);
    line-height: 1em;
    text-shadow: 3px 5px 1px rgb(12, 27, 168);
    -webkit-text-stroke-color: rgb(3, 12, 247);
    -webkit-text-stroke-width: 3px;
    margin-bottom: 20px;
    margin-top: 20px;
    text-align: center;
    

}
body {
  display: flex;
  background: red;
  align-self: auto;
  justify-content: center;
}
#app {
  font-family: monospace;
  text-align: center;
}
.viewer {
  float: left;
  opacity: 0.8;
  background-image: url("./assets/scanlines.jpg");
  height: 700px;
  width: 60%;
  border: 10px;
  border-style: solid;
}

.list {
  background: rgb(240, 240, 178);
  float: left;
  overflow-y: auto;
  height: 700px;
  max-width: 35%;
  border: 10px;
  border-style: solid;
}
</style>
