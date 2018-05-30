<template>
  <div>
    <h1>List of Ipsums ({{list.length}})</h1>
    <ul>
      <li
      v-for="ipsums in list"
      v-bind:key="ipsums.author"
      v-on:click="$emit('select', ipsums)"
      >
        <article v-bind:class="['ipsums', { selected: ipsums === selected }]">
          <strong>{{ipsums.author}}</strong>: 
          <em>{{ipsums.title}}</em>
        </article>
      </li>
    </ul>
  </div>
</template>

<script>
import ipsums from '../ipsums.js';

export default {
  data() {
    return {
      list: ipsums
    }
  },
  props: ['selected']
};
</script>
<style scoped>
  ul {
    list-style-type: none;
  }
  li:hover {
    cursor: pointer;
    background-color: lightcyan;
  }

</style>