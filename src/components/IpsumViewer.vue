<template>
  <div>
    <article class="ipsum-detail" v-if="ipsum">
      <h3>{{ipsum.pokemon}}</h3>
      <img v-bind:src="pokemon.url_image">
    </article>
    <p v-else>Please select an ipsum</p>
  </div>
</template>

<script>

export default {
  props: ['ipsum']
};

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.pokemon-detail {
  padding: 10px;
  text-align: center;
}

</style>
