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

div {
    background-color: lightblue;
    
}
h1 {
  font-size: 20pt;
    text-align: center;
    background-color: coral;
    width: 300px;
    height: 40px;
    margin: auto;
     
    border-radius: 30px 30px 30px 30px
}
h3 {
  display: flex;
  text-align: center;
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
  background:aqua;
   border-radius: 20px 20px 20px 20px
}
.ipsum.selected:hover {
  background: aquamarine;
   border-radius: 20px 20px 20px 20px
}
.ipsum:hover {
  background: aquamarine;
  border-radius: 20px 20px 20px 20px
}
.ipsum img {
  width: 75px;
  margin-right: 5px;
}
</style>