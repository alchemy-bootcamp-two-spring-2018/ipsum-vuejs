<template class="mainViewer">
    <div>
        <article v-if="pokemon">
            <img class="pokemonImage" v-bind:src="pokemon.url_image">
            <h2>{{pokemon.pokemon.toUpperCase()}}</h2>
            <p>Types: {{pokemon.type_1.toUpperCase()}}, {{pokemon.type_2.toUpperCase()}}</p>
            <p>HP: {{pokemon.hp}}</p>
            <p>Attack: {{pokemon.attack}}</p>
            <p>Defense: {{pokemon.defense}}</p>
            <a v-bind:href="pokemon.pokedex">More Info at Pokémon.com!</a>
        </article>
        <span class="startText" v-else>Welcome Trainer! Please Choose a Pokémon.</span>
    </div>
</template>

<script>

export default {
    props: ['pokemon']
};

</script>

<style>
.mainViewer {
    text-align: center; 
    float: left;
}

.pokemonImage {
    width: 400px;
    opacity: 0.7;
}

p {
    font-weight: bold;
    font-size: 15px;
}

a {
    font-weight: bold;
    font-size: 15px;
}
.startText {
    display: flex;
    margin-top: 200px;
    font-weight: bold;
    font-size: 50px;
}
    
</style>