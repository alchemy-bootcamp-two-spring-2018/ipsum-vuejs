<template>
  <div id="app">
    <h1>Lormpble Schpipshummz</h1>
    <div id="main">
      <section>
        <IpsumList class="list border"
          :selected ="selected"
          @select="updateSelected"
        />
      </section>
      <section>
        <IpsumViewer class="viewer border"
          v-bind:selected="selected"
        />
      </section>
    </div>
  </div>
</template>

<script>
import IpsumList from './components/IpsumList.vue';
import IpsumViewer from './components/IpsumViewer.vue';

export default {
  data() {
    return {
      selected: null,
    }
  },
  components: {
    IpsumList,
    IpsumViewer
  },
  methods: {
    updateSelected(selected) {
      console.log('jhhhkgkhj');
      this.selected = selected;
    }
  }
}
</script>

<style>
#main {
  display: flex;
  justify-content: space-between;
  text-shadow: 0 0 33px cyan;
  word-wrap: normal;
}

h1 {
  text-align: center;
  color: white;
}

.border {
  border-top: 5px solid gray;
  border-right: 5px solid black;
  border-bottom: 5px solid black;
  border-left: 5px solid gray;
  padding: 6px;
  margin: 0;
}

.list {
  display: inline-block;
  width: 222px;
  max-height: 400px;
  overflow: auto;
}

.viewer {
  display: inline-block;
  max-width: 555px;
  max-height: 400px;
  overflow: auto;
}
</style>
