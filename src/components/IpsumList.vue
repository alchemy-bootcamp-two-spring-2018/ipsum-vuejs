<template>
  <div> 
    <h1>List of Ipsum ({{list.length}})</h1>
    <ul>
      <li 
        v-for="ipsum in list"
        v-bind:key="ipsum.title"
        v-on:click="$emit('selected', ipsum)"
        v-bind:class="['ipsum', { selected: selected === ipsum }]">
        <article v-bind:class="['ipsum', { selected: ipsum === selected }]">
          <span>
            {{ipsum.title, ipsum.author}}
          </span>
        </article>
      </li>
    </ul>
  </div>
</template>
    
<script>
import ipsum from './ipsum.js';


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
.ipsum {
  display: flex;
  align-items: center;
  padding: 5px;
  cursor: pointer;
}
.ipsum.selected {
  background: antiquewhite;
}
.ipsum.selected:hover {
  background: wheat;
}
.ipsum:hover {
  background: steelblue;
}
.ipsum img {
  width: 75px;
  margin-right: 5px;
}
</style>