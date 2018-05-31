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
      this.selected = selected;
    }
  }
}
</script>

<style>
#main {
  display: flex;
  justify-content: space-around;
  align-items: center;
  text-shadow: 0 0 33px white;
  word-wrap: normal;
}

h1 {
  text-align: center;
  text-shadow: 1px 1px 3px black;
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
