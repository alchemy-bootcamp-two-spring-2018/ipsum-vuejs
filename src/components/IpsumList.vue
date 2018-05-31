<template>
  <div>
    <h1>List of Ipsums ({{list.length}})</h1>
    <hr>
    <ul>
      <li
      v-for="ipsums in list"
      v-bind:key="ipsums.author"
      v-on:click="$emit('select', ipsums)"
      >
        <article v-bind:class="['ipsums', { selected: ipsums === selected }]">
          <img v-bind:src="ipsums.image" class="icon">
          <div id="list-text">
            <strong>{{ipsums.author}}</strong>:
            <em>{{ipsums.title}}</em>
          </div>
        </article>
      </li>
    </ul>
  </div>
</template>

<script>
  import ipsums from '../ipsums.js';

  export default {
    data() {
      return {
        list: ipsums
      }
    },
    props: ['selected']
  };
</script>
<style scoped>
    h1 {
      margin-bottom: 0px;
    }
    #list-text {
      margin-left: 5px;
      margin-right: 3px;
    }
    hr {
      margin-bottom: 0px;
    }
    .selected {
      background: rgba(32, 178, 171, 0.432);
    }
    ul {
      list-style-type: none;
      padding-left: 2px;  
      height: 590px;;
      scroll-behavior: smooth;
      overflow-y: auto;
      margin-top: 0px;
      margin-bottom: 2px;

    
    }
    article {
      padding-top: 5px;
      padding-bottom:5px;
      display: flex;
      align-items:center;

    }
    li:nth-child(odd) {
      background: rgb(200, 210, 223);
    }
    li:hover {
      cursor: pointer;
      background-color: lightcyan;
    }
    .icon {
      width: 50px;
    }
</style>