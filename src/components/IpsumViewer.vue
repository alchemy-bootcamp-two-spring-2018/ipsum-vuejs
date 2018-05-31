<template>
  <div class="ipsum-detail">
    <article class="ipsum-detail" v-if="ipsum">
      <img v-bind:src="ipsum.image">
      <h2>Title: {{ipsum.title}}</h2>
      <h3>Author: {{ipsum.author}}</h3>
      <p>{{ipsum.body}}</p>
    </article>
    <p v-else >Choose an Ipsum</p>
  </div>
</template>

<script>
export default {
  props: ['ipsum']
};
</script>

<style scoped>

img {
  margin-top: 20px;
  width: 400px;
}
h2 {
  margin: 2px;
}
h3 {
  margin: 2px;
}
p {
  width: 80%;
}
.ipsum-detail {
  height: 650px;
  overflow-y: auto;
  margin-top: 8px;
  background-color: lightsteelblue;
  display: flex;
  flex-direction: column;
  align-items: center;
}

</style>