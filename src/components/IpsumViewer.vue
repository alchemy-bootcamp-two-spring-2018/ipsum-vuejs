<template>
  <div>
    <article v-if="ipsum">
      <h3>{{ipsum.title}}</h3>
      <ul>
          <li> {{ipsum.author}} </li>
          <li v-html='ipsum.body'> </li> 
      </ul>
    </article>
    <p v-else>Please select an ipsum</p>
  </div>
</template>

<script>

export default {
    data: {foo: 'foo'},
  props: ['ipsum']
};

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

/* .ipsum-detail {
  padding: 10px;
  text-align: center;
} */

</style>
