<template>
  <div>
    <h1>List of Ipsums</h1>
    <ul>
      <li
        v-for="ipsum in list"
        v-bind:key="ipsum.title"
        v-on:click="$emit('select', ipsum)"
      >
        <section v-bind:class="['ipsum', { selected: ipsum === selected }]">
          <span>{{ipsum.title}}</span>
        </section>
      </li>
    </ul>
  </div>
</template>

<script>
import ipsum from '../ipsums.js'

export default {
  data() {
    return {
      list: ipsum
    }
  },
  props: ['selected']
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
ul {
  list-style-type: none;
  padding: 0;
}
li {
  margin: 0 10px;
}
.ipsum {
  display: flex;
  align-items: center;
  padding: 5px;
  cursor: pointer;
}
.ipsum.selected {
  background: white;
}
.ipsum.selected:hover {
  background: aquamarine;
}
.ipsum:hover {
  background: aquamarine;
}
</style> 
