<template>
    <div class="viewer">
        <span v-if="selected">
            <h1>{{ selected.author }}</h1>
            <p v-html="selected.body"></p>
        </span>
        <h1 v-else>Plz select ipsumz</h1>
    </div>
</template>

<script>
    
export default {
    props: ['selected']
};

</script>

<style scoped>
div >>> img {
    max-height: 75px;
}
</style>