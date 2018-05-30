<template>
  <div id="app">
    <header>
      <h1>Pokemon Viewer</h1>
    </header>
    <main>
      <section class="list">
        <PokemonList/>
      </section>
      <section class="viewer"></section>
    </main>
  </div>
</template>

<script>
import PokemonList from './components/PokemonList.vue';

export default {
  name: 'app',
  components: {
    PokemonList
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

.list {
  /* max-height: 800px;
  overflow: auto; */
}
</style>
