<script>
	import NavigationBar from '$lib/components/navigation/NavigationBar.svelte';
	import '../app.css';
</script>

<div>
	<NavigationBar></NavigationBar>
	<main><slot></slot></main>
</div>

<style>
	div {
		display: flex;
		flex-direction: column-reverse;
		height: 100%;
	}

	main {
		flex-grow: 1;
		overflow-y: scroll;
	}
</style>
