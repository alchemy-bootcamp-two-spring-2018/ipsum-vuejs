<template>
  <div class="list">
    <h2>Ipsum List ({{ ipsumList.length }})</h2>
    <ul>
      <li
        v-for="ipsum in ipsumList"
        v-bind:key="ipsum.id"
        v-on:click="$emit('select', ipsum)"
        v-bind:class="{ chosenIpsum: ipsum === chosenIpsum }"
      >
      {{ ipsum.title }}
      </li>
    </ul>
  </div>
</template>

<script>
import ipsumList from '../data.js';

export default {
  data() {
    return {
      ipsumList: ipsumList
    }
  },
  props: ['chosenIpsum']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

h2 {
  padding-left: 10px;
}

ul {
  list-style: none;
  padding: 10px
}

li {
  cursor: pointer;
  line-height: 1.5em;
}

.chosenIpsum {
  color: blue;
  background: white;
}

</style>
