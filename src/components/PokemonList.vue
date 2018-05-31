<template>
  <div class="pokemon-list">
    
    <h2>Pokemon List - {{list.length}}</h2>
    
    <ul>
      <li 
        v-for="poke in list"
        v-bind:key="poke.id"
        v-on:click="$emit('select', poke)"
        v-bind:class="['pokemon', {selected: poke === selected}]"
      >
      {{poke.pokemon}}
      
      </li>
    </ul>

  </div>
</template>

<script>

import pokemon from '../pokemon.js';

export default {
  data () {
    return {
      list: pokemon
    }
  },
    
    props: ['selected']

  };

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

h2 {
  font-family: 'Nunito', sans-serif;
}

.pokemon {
  cursor: pointer;
}

.pokemon:hover {
  background: blanchedalmond;
  padding-left: 5px;
}

.pokemon.selected {
  background: lightgrey;
  padding-left: 5px;
}

ul {
  overflow-y: auto;
  height: 500px;
  font-size: 1.2em;
}

</style>
