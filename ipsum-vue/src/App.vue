<template>
  <div id="app">
    <header>
      <h1>Ipsum finder</h1>
      <p v-html="selectMessage"></p>
    </header>
    <main>
      <section class="list">
        <ipsum-list
        v-bind:selected="selected"
        v-on:select="updateSelected"
        />
      </section>

    </main>
  </div>
</template>

<script>
import IpsumList from './components/IpsumList.vue';

export default {
  data() {
    return {
      selected: null,
      selectMessage: '<span>Select an Ipsum</span>'
    }
  },
  components: {
    IpsumList
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
