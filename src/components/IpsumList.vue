<template>
  <div>
    <h1>Ipsum Options ({{list.length}})</h1>
    <ul>
      <li v-bind:class="['ipsumItem', { selected: ipsumItem === selected }]"
        v-for="ipsumItem in list"
        v-bind:key="ipsumItem.id"
        v-on:click="$emit('select', ipsumItem)"
      ><strong>{{ipsumItem.title}}</strong> - {{ipsumItem.category}}
        <!-- <article v-bind:class="['ipsumItem', { selected: ipsumItem === selected }]">
          <img v-bind:src="ipsumItem.url_image">
          <span v-bind:style="{ color: ipsumItem.color_1 }">
            {{ipsumItem.pokemon}}
          </span>
        </article> -->
      </li>
    </ul>
  </div>
</template>

<script>
import ipsumList from '../data.js';
export default {
  data() {
    return { 
      list: ipsumList 
    }
  },
  props: ['selected']
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  margin: 0 10px;
}
a {
  color: #42b983;
}
.ipsumItem {
  display: flex;
  align-items: center;
  padding: 5px;
  cursor: pointer;
}
.ipsumItem.selected {
  background: antiquewhite;
}
.ipsumItem.selected:hover {
  background: wheat;
}
.ipsumItem:hover {
  background: steelblue;
}
/* .ipsumItem img {
  width: 75px;
  margin-right: 5px;
} */
</style>