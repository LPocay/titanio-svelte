<script lang="ts">
	import { browser } from '$app/environment';
	import { page } from '$app/state';
	import Contact from '$lib/Contact.svelte';
	import Intro from '$lib/Intro.svelte';
	import Product from '$lib/Product.svelte';
	import Story from '$lib/Story.svelte';
	import Testimonials from '$lib/Testimonials.svelte';
	import { onMount } from 'svelte';

	if (browser) {
		onMount(() => {
			const hash = page.url.hash;
			if (hash) {
				const el = document.querySelector(hash);
				if (el) {
					setTimeout(() => {
						el.scrollIntoView({ behavior: 'smooth' });
					}, 200);
				}
			}
		});
	}
</script>

<main>
	<Intro />
	<Product />
	<Story />
	<Testimonials />
	<Contact />
</main>
