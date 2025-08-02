<script lang="ts">
	import { browser } from '$app/environment';
	import Loader from '$lib/Loader.svelte';
	import '../app.css';
	import Lenis from 'lenis';

	let { children } = $props();

	if (browser) {
		new Lenis({
			autoRaf: true
		});
	}

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

{#if isLoading}
	<Loader />
{/if}

{@render children()}
