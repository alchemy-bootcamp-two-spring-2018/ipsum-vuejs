<template>
  <div>
      <article v-if='ipsum'>
          <h1>{{ipsum.title}}</h1>
          <h4>Category: {{ipsum.category}}</h4>
          <h4>Author: {{ipsum.author}}</h4>
          <h4>Date Published: {{ipsum.publishedOn}}</h4>
          <p v-html='ipsum.body'>

              </p>
              
      </article>
    <p v-else>Please select a lorem ipsum to sample</p>
  </div>
</template>

<script>

export default {
    props: ['ipsum']
};

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1{
    font-size: 2.0em;
}

h4{
    display: inline;
    margin-right: 40px;
}

</style>
