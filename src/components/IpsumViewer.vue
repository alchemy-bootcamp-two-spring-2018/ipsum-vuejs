<template>
	<div>
  	<article class="ipsum-detail" v-if="importedItem">
    	<h3>{{importedItem.title}}</h3>
    	<ul>
				<li>Author: {{importedItem.author}}</li>
				<li>Author URL: {{importedItem.authorUrl}}</li>
				<li>Category: {{importedItem.category}}</li>
  		</ul>
    	<p><strong>Example: </strong><br>
    	<span class="block" v-html="importedItem.body"></span></p>;
    </article>

    <p v-else>Please select an Ipsum!</p>
  </div>
</template>

<script>
		export default {
			props: ['importedItem']
	};

</script>

<style scoped>

	h1 {
		font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
		font-size: 3em;
}

h2 {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    font-size: 2.0em;
    color: rgba(0, 0, 0 , .5);
}

h3 {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    font-size: 2.0em;
    color: rgba(0, 0, 0 , .7);
}

ul {
    list-style: none;
    padding: 4px;
    line-height: 2.5em;
    padding-left: 10px;
}

li {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    font-size: 1.3em;
}

li:hover {
background-color: aquamarine;
}

p{
 font-family: sans-serif;
    font-size: 1.3em;
}

img {
    display: block;
    border: 2px solid red;
    clear: both;
    margin: 20px;
    width: 300px;
}
</style>
