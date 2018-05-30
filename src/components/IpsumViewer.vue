<template>
  <div>
      <article v-if='ipsum'>
          <h3>{{ipsum.title}}</h3>
          {{ipsum.body}}
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


</style>
