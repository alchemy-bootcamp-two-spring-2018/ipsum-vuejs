<template>
<div id="app">
    <header>
        <h1> Ipsum Factum</h1>
    <hr>
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

<style scoped>
header {
    background: lightsteelblue;
    margin: -8px;
    padding-top: 10px;
    font-size: 40px;
    font-family: cursive;
}
h1 {
    margin: 0px;

}
hr {
    margin:3px;

}
.list {
    float: left;
    max-width: 300px;
    background: rgba(176, 196, 222, 0.836);
    text-align: center;
    margin-left: -8px;
}
.viewer {

    text-align: center;
}
#app {
    text-align: center;
    width: auto;
}
</style>
