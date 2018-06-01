<template>
    <div>
        <article class="ipsum-detail" v-if="ipsum">
            <h3>{{ipsum.title}}</h3>
            <ul>
                <li> {{ipsum.author}} </li>
                <li v-html='ipsum.body'> </li>
            </ul>
        </article>
        <p v-else> <strong>Please select an ipsum</strong></p>
    </div>
</template>

<script>
export default {
    props: ['ipsum']
};
</script>

<style scoped>
p {
    font-size: 20pt;
    text-align: center;
    background-color: orangered;
    width: 300px;
    height: 40px;
    margin: auto;
    border-radius: 30px 30px 30px 30px
    
}
.ipsum-detail {
background-color: aqua;
text-align: center;
border: black;
border-width: 5px;
border-radius: 30px 30px 30px 30px
}
</style>