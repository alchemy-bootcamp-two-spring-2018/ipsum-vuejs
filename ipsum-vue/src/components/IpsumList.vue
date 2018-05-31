<template>
    <div>
        <h1>List of Ipsums: {{list.length}}</h1>
        <ul>
            <li class="ipsum-list"
            v-for="ipsum in list"
            v-bind:key="ipsum.title"
            v-on:click="$emit('select', ipsum)"
            >
                <article>
                    <span>{{ipsum.title}}</span>
                </article>
            </li>
        </ul>
    </div>
</template>

<script>
import ipsum from '../data.js';

export default {
    data() {
        return {
            list: ipsum
        }
    },
    props: ['choice']
};
</script>


