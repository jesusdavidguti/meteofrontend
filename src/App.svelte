<script>
	import Nav from './Nav.svelte';
	import Contenido 	from './Contenido.svelte';
	import {Router}		from 'svelte-routing';
</script>

<style>
	@import url("https://fonts.googleapis.com/css?family=Aclonica");

	:global(*) {
		margin: 0;
		padding: 0;
	}

	:global(body) {
		display: flex;
		flex-direction: column;
		font-family: "Aclonica";
	}
	
	:global(a:hover) {
		text-decoration: none;
		cursor: pointer;
	}
</style>

<h1>meteofrontend</h1>

<Router>
	<Nav/>
	<Contenido/>
</Router>



