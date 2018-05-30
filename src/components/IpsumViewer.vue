<template>
  <div>
    <article class="ipsum-detail" v-if="ipsum">
      <h3>{{ipsum.ipsum}}</h3>
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
