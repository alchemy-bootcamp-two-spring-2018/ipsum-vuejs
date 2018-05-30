<template>
  <div>
    <article class="ipsum-detail" v-if="ipsum">
      <h3>{{ipsum.title}}</h3>
      <p v-html="ipsum.body"></p>
    </article>
    <p v-else>Please select an ipsum</p>
  </div>
</template>

<script>
export default {
  props: ['ipsum']
};
</script>

<style scoped>
div {
  padding: 10px;
}

div >>> img {
  display: block;
  max-height: 400px;
  padding-top: 10px;
  padding-bottom: 10px;
}
</style>
