<script lang="ts">
	let { children, href } = $props();
</script>

<div>
	<a
		{href}
		class="flex w-fit gap-1 rounded-3xl border border-solid border-white p-3 font-inter text-xs whitespace-nowrap text-white md:gap-2 md:text-[16px]"
	>
		{@render children()}
		<img src="/img/button-arrow.svg" alt="" />
	</a>
</div>
