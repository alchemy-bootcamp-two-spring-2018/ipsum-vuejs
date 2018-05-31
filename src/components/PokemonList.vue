<template>
    <div>
        <h2>Pokémon Captured: {{list.length}} </h2>
        <ul>
            <li
                class="listItems"
                v-for="pokemon in list"
                v-bind:key="pokemon.id"
                v-on:click="$emit('select', pokemon)"
            >
                <article v-bind:class="['pokemon', { selected: pokemon === selected }]">
                    <img v-bind:src="pokemon.url_image">
                    <span class="pokemonName">
                        {{pokemon.pokemon}}
                    </span>
                </article>
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

<style>
.pokemon {
    cursor: pointer;
    display: flex;
    align-items: center;

}
.pokemon img {

    width: 75px;
    margin-right: 5px;
    
}
.listItems {
    list-style: none;
}
.pokemonName {
    font-weight: bold;
}
.pokemon.selected {
  background: rgb(252, 176, 69);
}
.pokemon:hover {
  background: rgb(240, 227, 209);
}
</style>
