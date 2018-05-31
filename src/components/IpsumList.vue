<template>
  <div class="list">
    <ol>
      <li
        v-for="name in list"
        @click="$emit('select', name)"
        v-bind:key="name.author"
        v-bind:class="{ selected: name === selected }"
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
@keyframes selected-glow {
  from {
    background-position-x: 0;
  } to {
    background-position-x: 100%;
  }
}

@keyframes glow {
  from {
    background: cyan;
  } to {
    background: steelblue;
  }
}

li {
  padding: 3px;
  width: fit-content;
  border-radius: 3px;
  background-size: 200% 200%;
  animation: glow 1s alternate ease-in-out infinite;
  list-style: radial-gradient(cyan, darkcyan);
}

li:hover {
  background: cyan;
  cursor: pointer;
  font-weight: bold;
  animation: none;
}

.selected {
  background: linear-gradient(270deg, darkgoldenrod, gold);
  background-size: 200% 200%;
  animation: selected-glow 1s alternate ease-in-out infinite;
  list-style: radial-gradient(gold, darkgoldenrod);
}

.selected:hover {
  background: gold;
}
</style>
