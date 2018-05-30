<template>
  <div>
    <h1>{{list.length}} Ipsums</h1>
    <ul>
      <li
        v-for="ipsum in list"
        v-bind:key="ipsum.author"
        v-on:click="$emit('select', ipsum)"
      >
      <article v-bind:class="['ipsum', {selected: ipsum === selected }]">
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

<style>
  ul {
    list-style-type: none;
    padding: 0;
  }
</style>
