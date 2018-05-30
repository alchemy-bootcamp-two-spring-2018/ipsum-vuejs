<template>
    <div>
        <h1>Pokémon Captured: {{list.length}} </h1>
        <ul>
            <li
            v-for="pokemon in list"
            v-bind:key="pokemon.id"
            
            >
            <span>
            {{pokemon.pokemon}}
          </span>
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
    }
};
</script>

<style scoped>

</style>
