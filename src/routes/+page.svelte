<script lang="ts">
	import { browser } from '$app/environment';
	import Intro from '$lib/Intro.svelte';
	import Loader from '$lib/Loader.svelte';
	import Product from '$lib/Product.svelte';
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
	<Intro />
	<Product />
</main>
