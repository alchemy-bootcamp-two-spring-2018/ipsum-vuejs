<template>
<div>
  <h1>Lorem Ipsum Selector</h1>
  <h2>Choose from {{ipsum.length}} options!</h2>
  <ul>
    <li 
      v-for="ipsum in ipsum"
      v-bind:key = "ipsum.title"
      v-on:click="$emit('select', title)"
      >
      <article v-bind:class="['ipsum', { selected: title === selected }]">
        {{ipsum.title}}</article> <!-- might need to wrap this in a span class -->
        </li>
        </ul>
        </div>
        </template>

        <script>
        import ipsum from '../ipsumData.js'

export default {
  data() {
    return {
      ipsum: title

    }
  },
  props: ['selected']
};
</script>

<style scoped>

h1 {
font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
font-size: 3em;
}
h2 {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    font-size: 2.0em;
    color: rgba(0, 0, 0 , .5);
}
h3{
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    font-size: 2.0em;
    color: rgba(0, 0, 0 , .7);

}

ul {
    list-style: none;
    padding: 4px;
    line-height: 2.5em;
    padding-left: 10px;
}
li {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    font-size: 1.3em;

}
li:hover {
background-color: aquamarine;
}

p{
 font-family: sans-serif;
    font-size: 1.3em;
}
img {
    display: block;
    margin: 10px;
    max-height: 300px;
}


</style>
