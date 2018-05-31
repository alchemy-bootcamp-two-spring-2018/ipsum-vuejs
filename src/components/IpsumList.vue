<template>  
  <div>
      <h1>List o' Ipsums</h1>
      <ul>
          <li
            v-for="ipsum in list"
            v-bind:key="ipsum.title"

            v-on:click="$emit('select', ipsum)"
          >

          <article v-bind:class="['ipsum', { selected: ipsum === selected }]">

              <span v-bind:style="{ ????? }">
                  {{ipsum.ipsum}}
            </span>
          </article>

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

<style scoped>

ul {
    list-style: none;
    padding: 0;
}

li {
    margin: 0 14px;
}

.ipsum {
    display: flex;
    align-items: center;
    padding: 8px;
}

.ipsum.selected {
    background: lightblue;
}

.ipsum.selected:hover {
    background: mediumturquoise;
}

.ipsum:hover {
    background: steelblue;
}
</style>



