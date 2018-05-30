<template>
  <div class="list">
    <ol>
      <li
        v-for="name in list"
        @click="$emit('select', name)"
        v-bind:key="name.author"
        >{{ name.title }}</li>
    </ol>
  </div>
</template>

<script>
import ipsums from '../assets/data.js';

export default {
  data() {
    return {
      list: ipsums
    }
  },
  props: ['selected']
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
li:hover {
  background-color: cyan;
  cursor: pointer;
}
</style>
