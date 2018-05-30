<template>
    <div>
        <article class="mainViewer" v-if="pokemon">
            <img v-bind:src="pokemon.url_image">
            <h2>{{pokemon.pokemon.toUpperCase()}}</h2>
            <p>Types: {{pokemon.type_1.toUpperCase()}}, {{pokemon.type_2.toUpperCase()}}</p>
            <p>HP: {{pokemon.hp}}</p>
            <p>Attack: {{pokemon.attack}}</p>
            <p>Defense: {{pokemon.defense}}</p>
            <a v-bind:href="pokemon.pokedex">More Info at Pokémon.com!</a>
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
.mainViewer {
text-align: center;    
}

.mainViewer img {
    width: 400px;
    /* opacity: 50%; */
}
</style>