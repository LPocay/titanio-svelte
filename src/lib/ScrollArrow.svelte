<script lang="ts">
	let { position } = $props<{ position: 'right' | 'left' }>();
</script>

{#if position === 'left'}
	<div class="absolute left-8 bottom-8">
		<img src="/img/scroll-arrow.svg" alt="" />
	</div>
{:else}
	<div class="absolute right-8 bottom-8">
		<img src="/img/scroll-arrow.svg" alt="" />
	</div>
{/if}
