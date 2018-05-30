<template>
  <div>
    <h1>Select An Ipsum To Preview:</h1>
    <ul>
      <li 
          v-for="title in list"
          v-bind:key="title"
          v-on:click="$emit('select', title)"
      >
        <article v-bind:class="['title', { selected: title === selected }]">
        </article>
      </li>
    </ul>
  </div>
</template>