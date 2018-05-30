<template>
<div id="app">
    <header>
        <h1> Ipsum Factum Viewer</h1>
    </header>
    <main>
        <section class="list">
            <IpsumList
            v-bind:selected="selected"
            v-on:select="UpdateSelected"
            />
        </section>
        <section class="viewer">
            <IpsumViewer v-bind:ipsum="selected"/>
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
            selected: null
        }
    },
    components: {
        IpsumList,
        IpsumViewer
    },
    methods: {
        UpdateSelected(ipsum) {
            this.selected = ipsum;
            console.log(this.selected.author);
        }
    }
};

</script>

<style>

</style>
