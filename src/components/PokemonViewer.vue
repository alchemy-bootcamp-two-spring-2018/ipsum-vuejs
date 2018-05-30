<template>
  <div class="content">
      <span class="viewer" v-if="pokemon">
        <h2>{{pokemon.pokemon}}</h2>
        <img v-bind:src="pokemon.url_image">
        <ul>
          <li>Type 1: {{pokemon.type_1}}</li>
          <li>Type 2: {{pokemon.type_2}}</li>
          <li>HP: {{pokemon.hp}}</li>
          <li>Attack: {{pokemon.attack}}</li>
          <li>Defense: {{pokemon.defense}}</li>
          <li>Speed: {{pokemon.speed}}</li>
          <li>Special Attack: {{pokemon.special_attack}}</li>
          <li>Special Defense: {{pokemon.special_defense}}</li>
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
.content {
border: 2px solid black;
margin-left: 100px;
}

p, h2 {
  padding: 10px;
  text-align: center;
}

.viewer {
  text-transform: capitalize;
}

.viewer img {
  width: 400px;
}

ul {
  width: fit-content;
  text-align: left;
  list-style-type: none;
}

</style>
