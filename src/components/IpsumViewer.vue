<template>
  <div class="viewer">
    <section v-if="ipsum">
      <h2>{{ ipsum.title }}</h2>
      <h3>Category: {{ ipsum.category }}</h3>
      <h4>Author: <a :href="ipsum.authorUrl">{{ ipsum.author }}</a></h4>
      <p v-html="ipsum.body"></p>
      <h6>Published on {{ ipsum.publishedOn }}</h6>
    </section>
    <h2 v-else>Make a selection</h2>
  </div>
</template>

<script>
export default {
  props: ['ipsum']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.viewer {
  overflow: scroll;
}

h2 {
  margin: 0px;
}

p {
  text-align: justify;
}



</style>
