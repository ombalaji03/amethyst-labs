<script>
	import ContributorCard from '$lib/components/contributors/ContributorCard.svelte';
</script>

<div id="container">
	<ContributorCard name="Janan Patel" tags="owner developer designer writer"></ContributorCard>
	<ContributorCard></ContributorCard>
</div>

<style>
	#container {
		@apply p-4;
	}
</style>
