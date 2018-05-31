<template>
  
  <div>
    <section class="ipsum-viewer" v-if="ipsum">
      <h2>{{ipsum.title}}</h2>
      <h3>Category: {{ipsum.category}}</h3>
      <h3>Author: {{ipsum.author}}</h3>
      <p v-html="ipsum.body">{{ipsum.body}}</p>
    </section>
    <p v-else>Please Select an Ipsum to Preview</p>
  </div>

</template>

<script>
import ipsum from '../data.js'

export default {
  props: ['ipsum']
};

</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Neuton');

.ipsum-viewer {
  margin-top: -27px;
  padding-left: 40px;
}

h2 {
  font-family: 'Neuton', serif;
  font-size: 2em;
  color: white;
  padding: 20px;
  background-color: rgb(68, 54, 82);
}

h3 {
  color:  rgb(68, 54, 82);
}

img {
  display: none;
}

p {
  max-width: 600px;
}


</style>