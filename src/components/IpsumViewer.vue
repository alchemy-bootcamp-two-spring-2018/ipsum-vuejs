<template>
    <div>
        <article class="ipsum-detail" v-if="ipsum">
            <h3>{{ipsum.title}}</h3>
            <ul>
                <li> {{ipsum.author}} </li>
                <li v-html='ipsum.body'> </li>
            </ul>
                
            <!-- <div v-bind:src="ipsum.authorUrl"></div> -->
            <!-- <div>
            </div> -->

        </article>
        <p v-else>Please select an ipsum</p>
    </div>
</template>

<script>
export default {
    props: ['ipsum']

};

</script>

<style scoped>
.ipsum-detail {

padding: 10px;
text-align: center;

}

</style>
