<template>
  <div>
    <article class="ipsum-detail" v-if="ipsumItem">
      <h3>{{ipsumItem.title}}</h3>
      <ul>
        <li>Author: {{ipsumItem.author}}</li>
        <li>Category: {{ipsumItem.category}}</li>
        <li>Date Published: {{ipsumItem.publishedOn}}</li>
        <li>URL: {{ipsumItem.authorUrl}}</li>
      </ul>
      <!-- <img v-bind:src="ipsumItem.url_image"> -->
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
.ipsum-detail {
  padding: 10px;
  /* text-align: center; */
}
</style>