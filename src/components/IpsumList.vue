<template>
  <div>
    <h1>{{list.length}} Ipsums</h1>
    <ul>
      <li
        v-for="ipsums in list"
        v-bind:key="ipsums.author"
        v-on:click="$emit('select', ipsums)"
      >
      <article>{{ipsums.title}}</article>
      </li>
    </ul>
  </div>
</template>

<script>
import ipsums from '../data.js';

export default {
  data() {
    return {
      list: ipsums
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
