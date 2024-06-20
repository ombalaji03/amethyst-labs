<script>
	import NavigationButtons from './NavigationButtons.svelte';
</script>

<header>
	<nav>
		<NavigationButtons></NavigationButtons>
	</nav>
</header>

<style>
	header {
		@apply p-2 bg-gray-800 border-gray-700;
		border-top-width: 1px;
	}

	nav {
		display: flex;
		justify-content: space-around;
	}
</style>
