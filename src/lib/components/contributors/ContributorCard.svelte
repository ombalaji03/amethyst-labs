<script>
	import ContributorTags from './ContributorTags.svelte';

	export let imgSrc = 'https://wallpapers-clan.com/wp-content/uploads/2023/05/cool-pfp-02.jpg';
	export let name = 'Dummy';
	export let tags = 'dummy';
</script>

<div id="card">
	<img src={imgSrc} alt="" />
	<div id="content">
		<div id="name">{name}</div>
		<ContributorTags {tags}></ContributorTags>
	</div>
</div>

<style>
	#card {
		@apply mb-4 p-4 bg-gray-800 border-gray-700 rounded-lg shadow-lg;
		display: flex;
		border-top-width: 1px;
	}

	img {
		@apply w-32 h-32 mr-4 rounded-full;
	}

	#content {
		display: flex;
		flex-direction: column;
	}

	#name {
		@apply mb-2 text-gray-50 text-lg;
	}
</style>
