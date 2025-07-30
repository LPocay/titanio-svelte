<script lang="ts">
	import whiteArrow from '$lib/assets/link-arrow-white.svg';
	import blackArrow from '$lib/assets/link-arrow-black.svg';
	let { children, href, dark = false, big = false } = $props();
	const arrowImage = dark ? blackArrow : whiteArrow;
  const colors = dark ? "border-titanio-500 text-titanio-500" : "border-white text-white";
  const textSize = big ? "md:text-3xl" : "md:text-[16px]";
</script>

<div>
	<a
		{href}
		class={`flex w-fit gap-1 rounded-4xl border border-solid p-3 font-inter text-xs whitespace-nowrap md:gap-2 ${colors} ${textSize}`}
	>
		{@render children()}
		<img src={arrowImage} width={big ? 26 : 14} alt="" />
	</a>
</div>
