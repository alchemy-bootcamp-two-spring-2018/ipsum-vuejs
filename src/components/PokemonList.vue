<template>
    <div>
        <h1>Pokémon Captured: {{list.length}} </h1>
        <ul>
            <li
                v-for="pokemon in list"
                v-bind:key="pokemon.id"
                v-on:click="$emit('select', pokemon)"
            >
                <article v-bind:class="['pokemon', { selected: pokemon === selected }]">
                    <img v-bind:src="pokemon.url_image">
                    <span>
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
    }
    // props: ['selected']
};
</script>

<style scoped>

.pokemon img {
    display: block;
    width: 75px;
    margin-right: 5px;
}


</style>
