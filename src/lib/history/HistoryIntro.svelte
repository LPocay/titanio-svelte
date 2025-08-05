<script>
	import Nav from '$lib/Nav.svelte';
	import ScrollArrow from '../ScrollArrow.svelte';
</script>

<section
	class="relative h-screen bg-[url(/img/intro-bg.png)] bg-cover md:overflow-hidden md:bg-[url(/img/intro-big-bg.png)]"
>
	<Nav />
	<ScrollArrow position="right" />
	<div
		class="flex h-full flex-col items-center justify-center pt-1 text-white md:absolute md:bottom-[-22px] md:items-start md:justify-end md:pl-14"
	>
		<div class="px-16 md:px-0">
			<h1 class="text-left font-inter md:text-[44px]">Nuestra hisoria</h1>
			<h1 class="text-left font-gabarito text-3xl font-extrabold uppercase md:text-[74px]">
				MÁS DE 50 AÑOS EN EL MERCADO
			</h1>
		</div>
	</div>
</section>
