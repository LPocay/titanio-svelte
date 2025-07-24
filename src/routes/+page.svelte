<script lang="ts">
	import { browser } from '$app/environment';
	import Loader from '$lib/Loader.svelte';
	let isLoading = $state(true);
	if (browser) {
		if (document.readyState === 'complete') {
			isLoading = false;
		} else {
			window.addEventListener('load', () => {
				isLoading = false;
			});
		}
	}
</script>

<main>
	{#if isLoading}
		<Loader />
	{/if}
	<section></section>
</main>
