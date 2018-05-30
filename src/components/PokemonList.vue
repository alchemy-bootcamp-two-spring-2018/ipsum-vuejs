<template>
  <div>
    <h1>Check out one of the {{list.length}} pokemon!</h1>
    <ul>
        <li
          v-for="pokemon in list"
          v-bind:key="pokemon.id"
          v-on:click="$emit('select', pokemon)"
        >
        <div v-bind:class="['pokemon-li', { selected: pokemon === selected }]">
          <img v-bind:src="pokemon.url_image">
          {{pokemon.pokemon}}
        </div>
        </li>
    </ul>
  </div>
</template>

<script>
import pokemon from '../pokemon.js';

export default {
  data() {
    return {
      list: pokemon
    }
  },
  props: ['selected']
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  margin-left: 20px;
}

ul {
   list-style-type: none;
   height: 600px;
   overflow-y: auto;
}

.pokemon-li {
  display: flex;
  align-items: center;
  text-transform: capitalize;
  width: 275px;
}

li:nth-child(odd) {
  background: rgba(243, 203, 181, 0.466);
  width: 275px;
  }


  .pokemon-li:hover {
    background-color: peachpuff;
    cursor: pointer;
  }

.pokemon-li.selected {
  background-color: rgb(238, 170, 170);
}

.pokemon-li.selected:hover {
  background-color: rgb(238, 142, 142);
}

.pokemon-li img {
  width: 100px;
  padding-right: 15px;
}

</style>
