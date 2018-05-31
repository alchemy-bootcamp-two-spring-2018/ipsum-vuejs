<template>  
  <div>
      <h3>Earth's Hottest Ipsums</h3>
      <ul>
          <li
            v-for="ipsum in list"
            v-bind:key="ipsum.title"

            v-on:click="$emit('select', ipsum)"
          >

          <article v-bind:class="['ipsum', { selected: ipsum === selected }]">

              <span>
                  {{ipsum.title}}
            </span>
          </article>
        </li>
      </ul>
  </div>  
</template>

<script>
import ipsum from '../data/ipsums.js';

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

h3 {
    font-size: 18px;
    text-align: center;
    text-decoration-color: maroon;
    text-decoration-line: overline;
    background-color: #fbead1;
    margin-top: 0px;
    margin-right: 160px;
    margin-left: 160px;
    padding-top: 0px;
    padding-bottom: 10px;
    border-radius: 0px 0px 20px 20px;
}

ul {
    list-style: none;
    padding: 60;
}

li {
    margin: 0 20px;
    width: fit-content;
    display: inline-block; 
    font-weight:500;  
}

.ipsum {
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



