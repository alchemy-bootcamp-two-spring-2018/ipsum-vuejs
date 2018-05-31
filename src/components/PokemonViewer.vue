<template>
  <div class="pokemon-viewer">

    <section v-if="pokemon">
      <h2>{{pokemon.pokemon.toUpperCase()}}</h2>
      <img v-bind:src="pokemon.url_image"/>
      <h3>type - {{pokemon.type_1}}</h3>
    </section>
    
    <p v-else>Select a Pokemon</p>

  </div>
</template>

<script>

export default {
  props: ['pokemon']
};

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

h2 {
  text-align: center;
}

img {
  width: 350px;
}

h3 {
  text-align: center;
}

</style>