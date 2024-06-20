<script>
	export let tags = 'dummy';
	const tagsArray = tags.split(' ');
</script>

<div id="container">
	{#each tagsArray as tag}
		{#if tag === 'owner'}
			<div class="tag bg-red-950 border-red-400 text-red-400">Owner</div>
		{:else if tag === 'professor'}
			<div class="tag bg-orange-950 border-orange-400 text-orange-400">Profesor</div>
		{:else if tag === 'developer'}
			<div class="tag bg-blue-950 border-blue-400 text-blue-400">Developer</div>
		{:else if tag === 'designer'}
			<div class="tag bg-pink-950 border-pink-400 text-pink-400">Designer</div>
		{:else if tag === 'writer'}
			<div class="tag bg-green-950 border-green-400 text-green-400">Writer</div>
		{:else}
			<div class="tag bg-yellow-950 border-yellow-400 text-yellow-400">Dummy</div>
		{/if}
	{/each}
</div>

<style>
	#container {
		@apply gap-1;
		display: flex;
		flex-wrap: wrap;
	}

	.tag {
		@apply px-1 text-sm rounded-md;
		text-align: center;
		border-width: 1px;
	}
</style>
