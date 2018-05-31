<template>
    <div>
        <article class="ipsum-info" v-if="ipsum">
            <h3>{{ipsum.title}}</h3>
            <ul>
                <li>Category: {{ipsum.category}}</li>
                <li>Author: {{ipsum.author}}</li>
                <li>Address: {{ipsum.authorUrl}}</li>
                <li>Published on: {{ipsum.publishedOn}}</li>
            </ul>
            <p v-html="ipsum.body"></p>
        </article>
        <section v-else>
            <h4>Please select an Ipsum from the list on the left</h4>
            <p class="ipsum-space">Ipsum here!</p>
        </section>
    </div>
</template>

<script>
export default {
    props: ['ipsum']
};
</script>

<style scoped>
h4 {
    text-align: center;
}

.ipsum-space {
    text-align: center;
}
</style>



