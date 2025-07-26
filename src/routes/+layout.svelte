<script lang="ts">
	import { browser } from '$app/environment';
	import '../app.css';
	import Lenis from 'lenis';

	let { children } = $props();

	if (browser) {
		new Lenis({
			autoRaf: true
		});
	}
</script>

{@render children()}
