<template>
  <div>
    <h1>List of Ipsums ({{list.length}})</h1>
    <ul>
      <li
      v-for="ipsums in list"
      v-bind:key="ipsums.author">
        <article v-bind:class="['ipsums']">
          {{ipsums.author}}
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

  }
};
</script>
<style scoped>
  ul {
    list-style-type: none;
    
  }
</style>