<script>
	import { goto } from '$app/navigation';
	import { base } from '$app/paths';
	import { page } from '$app/stores';

	function getActiveButton() {
		if ($page.url.pathname === '/contributors') return 'menu';
		else return 'home';
	}

	/**
	 * @param {string} buttonName
	 */
	function clickHandler(buttonName) {
		if (buttonName === 'home') handleHome();
		else if (buttonName === 'menu') handleMenu();
		// else if (buttonName === 'video_library') handleVideoLibrary();
		// else handleLibraryBooks();
	}

	function handleHome() {
		goto(`${base}/`);
	}

	function handleMenu() {
		goto(`${base}/contributors`);
	}

	// TODO

	// function handleVideoLibrary() {}

	// function handlelibraryBooks() {}

	let buttons = ['home', 'menu', 'video_library', 'library_books'];
	let activeButton = getActiveButton();
	let classList = 'active bg-gradient-to-r from-blue-500 via-sky-500 to-cyan-500 shadow-blue-500';
</script>

{#key activeButton}
	{#each buttons as button}
		<button
			on:click={function () {
				activeButton = button;
				clickHandler(button);
			}}
		>
			{#if button === activeButton}
				<span class="{classList} material-symbols-outlined"> {button} </span>
			{:else}
				<span class="material-symbols-outlined"> {button} </span>
			{/if}
		</button>
	{/each}
{/key}

<style>
	span {
		@apply p-2 text-gray-700;
	}

	.material-symbols-outlined {
		font-variation-settings:
			'FILL' 1,
			'wght' 400,
			'GRAD' 0,
			'opsz' 24;
	}

	.active {
		background-clip: text;
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
		text-shadow: 0px 10px 48px var(--tw-shadow-color);
	}
</style>
