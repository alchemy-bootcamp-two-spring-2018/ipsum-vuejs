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
      
      <section class="detail-viewer" v-bind:class="[{selected: selected !== null}]">
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
  font-family: 'Stalinist One', cursive;
  font-size: 4em;
  color: ivory;
  background-image: url("background.jpg");
  background-size: cover;
  height: 2.5em;
  margin: 0px 0px 30px 0px;

}

.list {
  border-top: solid;
  border-bottom: solid;
}

.detail-viewer.selected {
  border-style: solid;
  border-radius: 5px;
  padding: 5px;
  background-color: blanchedalmond;
}
</style>
