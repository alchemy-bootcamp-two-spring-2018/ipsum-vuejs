<template>
<div>
  <h3>Lorem Ipsum Selector</h3>
  <h2>Choose from {{importedList.length}} options!</h2>
  <ul>
    <li 
      v-for="importedItem in importedList"
      v-bind:key="importedItem.id"
      v-on:click="$emit('select', importedItem)"
      >
      <article v-bind:class="['ipsum', { selected: importedList === selected }]">
        {{importedItem.title}}</article> <!-- might need to wrap this in a span class -->
        </li>
        </ul>
        </div>
        </template>

        <script>
        import ipsumList from '../ipsumData.js'
        console.log(ipsumList);

export default {
  data() {
    return {
      importedList: ipsumList
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

.ipsum {
  display: flex;
  align-items: center;
  padding: 5px;
  cursor: pointer;
}


</style>
