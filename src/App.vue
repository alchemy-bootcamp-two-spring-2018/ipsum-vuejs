<template>
<div id="app">
    <header>
        <h1> Ipsum Factum Viewer</h1>
    </header>
    <main>
        <section class="list">
            <IpsumList
            v-bind:selected="selected"
            v-on:select="logConsole"
            />
        </section>
        <section class="viewer">
\            <IpsumViewer/>
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
        logConsole(selected) {
            this.selected = selected
            console.log(this.selected);
        }
    }
};

</script>

<style>

</style>
