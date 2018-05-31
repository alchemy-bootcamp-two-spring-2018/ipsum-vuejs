<template>
  <div>
    <section class="ipsum-detail" v-if="ipsum">
      <h1>{{ipsum.title}}</h1>
      <ul id="viewer">
        <li>Author: {{ipsum.author}}</li>
        <li>Category: {{ipsum.category}}</li>
        <li>Author Url: {{ipsum.authorUrl}}</li>
        <li>Published on: {{ipsum.publishedOn}}</li>
        <li v-html="ipsum.body">Text: {{ipsum.body}}</li>
      </ul>
      
    </section>
    <p v-else>Please select an ipsum to preview</p>
  </div>
</template>

<script>
import ipsum from '../ipsums.js'

export default {
  props: ['ipsum']
};
</script>

<style scoped>
ul {
  list-style-type: none;
  padding: 0;
}
img {
  display: none;
}
</style> 