<template>
<div id="app">
    <header>
        <h1> Ipsum Factum Viewer</h1>
    </header>
    <main>
        <section class="list">
            <IpsumList/>
        </section>
        <section class="viewer">
            viewer section
        </section>
    </main>

</div>
</template>

<script>
import IpsumList from './components/IpsumList.vue';

export default {
    
    components: {
        IpsumList
    }
};

</script>

<style>

</style>
