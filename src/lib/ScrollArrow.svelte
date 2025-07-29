<script lang="ts">
	import whiteArrow from '$lib/assets/scroll-arrow-white.svg';
	import blackArrow from '$lib/assets/scroll-arrow-black.svg';
	let { position, dark = false } = $props<{ position: 'right' | 'left'; dark?: boolean }>();
	const arrowImage = dark ? blackArrow : whiteArrow;
</script>

{#if position === 'left'}
	<div class="absolute bottom-8 left-8">
		<img src={arrowImage} alt="" class="md:h-32" />
	</div>
{:else}
	<div class="absolute right-8 bottom-8">
		<img src={arrowImage} alt="" class="md:h-32" />
	</div>
{/if}
