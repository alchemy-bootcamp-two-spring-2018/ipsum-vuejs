<template>
  <div>
    <article class="ipsum-detail" v-if="ipsumItem">
      <h3>{{ipsumItem.title}}</h3>
      <ul>
        <li><strong>Author: </strong>{{ipsumItem.author}}</li>
        <li><strong>Category: </strong>{{ipsumItem.category}}</li>
        <li><strong>Date Published: </strong>{{ipsumItem.publishedOn}}</li>
        <li><strong>URL: </strong><a v-bind:href="ipsumItem.authorUrl">{{ipsumItem.authorUrl}}</a></li>
      </ul>
      <p v-html="ipsumItem.body"></p>
    </article>
    <p v-else>Please select an Ipsum option</p>
  </div>
</template>

<script>
export default {
  props: ['ipsumItem']
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

ul {
  list-style: none;
}

/* it completely ignores my image styling.  Something about being in v-html? */
p img {
  width: 200px;
}

p {
  text-align: justify;
}

</style>