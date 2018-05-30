<template>
  <div>
      <span class="viewer" v-if="pokemon">
        <h2>{{pokemon.pokemon}}</h2>
        <img v-bind:src="pokemon.url_image">
        <ul>
          <li>Type 1: {{pokemon.type_1}}</li>
        </ul>
      </span>
      <p v-else>Select a pokemon to learn more!</p>
  </div>
</template>

<script>

export default {
  props: ['pokemon']
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
p, h2 {
  padding: 10px;
  text-align: center;
}

.viewer {
  text-transform: capitalize;
  text-align: center;
}

.viewer img {
  width: 400px;
}

ul {
  width: 100px;
}

</style>
