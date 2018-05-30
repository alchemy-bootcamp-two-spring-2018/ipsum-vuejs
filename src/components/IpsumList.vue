<template>
  <div>
    <h1>List of Ipsums ({{list.length}})</h1>
    <ul>
      <li></li>
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