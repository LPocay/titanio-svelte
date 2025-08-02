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
		class="flex h-full flex-col items-center justify-center pt-1 text-white md:items-start md:justify-end md:pl-14 md:absolute md:bottom-[-30px]"
	>
		<h1 class="font-inter md:text-[44px]">Como funciona</h1>
		<h1 class="font-gabarito text-6xl font-extrabold uppercase md:text-[180px]">Titanio</h1>
	</div>
</section>
