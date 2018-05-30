<template>
  <div id="app">
    
    <header>
      <h1>Pokemon Directory</h1>
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

h1 {
  text-align: center;
}
main {
  display: flex;
  justify-content: space-around;
}

</style>
