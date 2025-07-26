<script lang="ts">
	let { children } = $props();
</script>

<div>
	<a
		href=""
		class="flex w-fit gap-1 md:gap-2 rounded-3xl border border-solid border-white p-3 font-inter text-xs whitespace-nowrap text-white md:text-[16px]"
	>
		{@render children()}
		<img src="/img/button-arrow.svg" alt="" />
	</a>
</div>
