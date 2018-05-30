<template>
  <div>
    <h1>Check out one of the {{list.length}} pokemon!</h1>
    <ul>
        <li
          v-for="pokemon in list"
          v-bind:key="pokemon.id"
        >
        <div class="pokemon-li">
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
.pokemon-li {
  display: flex;
  align-items: center;
}

.pokemon-li img {
  width: 100px;
  padding-right: 15px;
}

</style>
