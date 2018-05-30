<template>
  <div>
    <h1>List of Ipsums ({{list.length}})</h1>
    <ul>
      <li
      v-for="ipsum in list"
      :key="ipsum.author"
      @click="$emit('select', ipsum)"

      >{{ ipsum.title }}</li>
    </ul>
  </div>
</template>

<script>
import ipsum from '../Ipsums.js'

export default {
  data() {
    return {
      list: ipsum
    }
  },

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.selected{
  color:red;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
