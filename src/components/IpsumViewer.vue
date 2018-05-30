<template>
  <div>
    <article class="ipsum-detail" v-if="ipsum">
      <img v-bind:src="ipsum.image">
      <h2>{{ipsum.title}}</h2>
    </article>
    <p v-else>Choose an Ipsum</p>
  </div>
</template>

<script>
export default {
  props: ['ipsum']
};
</script>

<style scoped>
</style>