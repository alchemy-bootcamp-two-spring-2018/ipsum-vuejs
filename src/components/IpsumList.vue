<template>
  <div class="list">
    <h2>Ipsum List ({{ ipsumList.length }})</h2>
    <ul>
      <li
        v-for="ipsum in ipsumList"
        v-bind:key="ipsum.id"
      >
      {{ ipsum.title }}
      </li>
    </ul>
  </div>
</template>

<script>
import ipsumList from '../data.js';

export default {
  data() {
    return {
      ipsumList: ipsumList
    }
  },
  props: {
    
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
