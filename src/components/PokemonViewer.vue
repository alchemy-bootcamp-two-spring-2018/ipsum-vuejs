<template>
    <div>
        <article v-if="pokemon">
            <img v-bind:src="pokemon.url_image">
            <h2>{{pokemon.pokemon.toUpperCase()}}</h2>
            <p>Types: {{pokemon.type_1.toUpperCase()}}, {{pokemon.type_2.toUpperCase()}}</p>
            <p>HP: {{pokemon.hp}}</p>
            <p>Attack: {{pokemon.attack}}</p>
            <p>Defense: {{pokemon.defense}}</p>
        </article>
        <p v-else>Welcome Trainer! Please Choose a Pokémon.</p>
    </div>
</template>

<script>

export default {
    props: ['pokemon']
};

</script>


<style scoped>
</style>