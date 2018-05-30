<template>
  <div>
    <h1>{{list.length}} Ipsums</h1>
    <ul>
      <li
        v-for="ipsum in list"
        :key="ipsum.author"
        @click="$emit('select', ipsum)"
      >
      <article :class="['ipsum', {selected: ipsum === selected }]">
        {{ipsum.title}}
      </article>
      </li>
    </ul>
  </div>
</template>

<script>
import ipsum from '../ipsums.js';

export default {
  data() {
    return {
      list: ipsum
    }
  },
  props: ['selected']
};
</script>

<style scoped>
div {
  padding: 10px;
}

ul {
  list-style-type: none;
  padding: 0;
}

li:hover {
  background: #eee;
  cursor: pointer;
}
</style>
