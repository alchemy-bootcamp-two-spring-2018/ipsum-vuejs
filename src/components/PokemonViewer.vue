<template>
  <div class="pokemon-viewer">

    <section v-if="pokemon">
      <h2>{{pokemon.pokemon}}</h2>
      <h3>type - {{pokemon.type_1}}</h3>
      <img v-bind:src="pokemon.url_image"/>
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

img {
  width: 250px;
}
</style>