<template>
  <div id="app">
    <header>
      <h1>Ipsum Viewer</h1>
      <p v-html="someHtml"></p>
    </header>


    <main>
      <section class="list">
        <IpsumList
          v-bind:selected="selected"
          v-on:selected="updateSelected"
          />
      </section>
      
      <section class="viewer">
        <IpsumViewer
        v-bind:ipsum="selected"
        />
      </section>
    </main>
  </div>
</template>

<script>
import IpsumList from './components/IpsumList.vue';
import IpsumViewer from './components/IpsumViewer.vue';

export default {
  data() {
    return {
      selected: null,
      someHtml: '<strong>Hello! Pick an Ipsum!</strong>'
    }
  },
  components: {
    IpsumList,
    IpsumViewer
  },
  methods: {
    updateSelected(ipsum) {
      this.selected = ipsum;
    }
  }
};
</script>


