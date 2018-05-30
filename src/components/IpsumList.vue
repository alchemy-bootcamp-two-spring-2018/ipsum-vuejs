<template>
  <div>
    <h1>List of Ipsum ({{list.length}})</h1>
    <ul>
      <li 
        v-for="ipsum in list"
        v-bind:key="ipsum.id"
        v-on:click="$emit('select', ipsum)"
      >
        <article v-bind:class="['ipsum', { selected: ipsum === selected }]">
          <img v-bind:src="pokemon.url_image">
          <span v-bind:style="{ color: pokemon.color_1 }">
            {{ipsum.title}}
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

/* .pokemon img {
  width: 75px;
  margin-right: 5px;
} */
</style>