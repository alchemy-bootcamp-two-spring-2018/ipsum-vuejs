<template>
    <div>
        <article class="ipsum-detail" v-if="ipsum">
            <h3>{{ipsum.title}}</h3>
            <h4>Category: {{ipsum.category}}</h4>
            <h4>Author: {{ipsum.author}}</h4>
            <h4>Author URL: {{ipsum.authorUrl}}</h4>
            <h4>Published On:{{ipsum.publishedOn}}</h4>
            <span v-html="ipsum.body"></span>
        </article>
        <p id="pick" v-else>Please select an ipsum!</p>

    </div>
</template>

<script>

export default {
    props: ['ipsum']
};

</script>

<style scoped>

.ipsum-detail {
    padding: 12px;
    text-align: center;
    margin-right: 120px;
    margin-left: 120px;  
}

#pick {
    text-align: center;
    font-weight: 800;
    font-size: 2em;
}

</style>