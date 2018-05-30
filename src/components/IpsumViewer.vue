<template>
  <div>
    <article class="ipsum-detail" v-if="ipsum">
      <h3>{{ipsum.title}}</h3>
      <p>{{ipsum.body}}</p>
    </article>
    <p v-else>Please select an ipsum</p>
  </div>
</template>

<script>
export default {
  props: ['ipsum']
};
</script>

<style>

</style>
