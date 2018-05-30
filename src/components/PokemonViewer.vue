<template>
    <div>
        <article v-if="pokemon">
            <h3>{{pokemon.pokemon}}</h3>
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