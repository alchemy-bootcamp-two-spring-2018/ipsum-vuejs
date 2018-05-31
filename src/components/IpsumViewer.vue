<template>
  
  <div>
    <section class="ipsum-viewer" v-if="ipsum">
      <h3>{{ipsum.title}}</h3>
      <h2>{{ipsum.category}}</h2>
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



</style>