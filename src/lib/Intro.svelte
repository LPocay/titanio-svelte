<script>
	import Nav from './Nav.svelte';
	import ScrollArrow from './ScrollArrow.svelte';
</script>

<section
	class="relative h-screen bg-[url(/img/intro-bg.png)] md:bg-[url(/img/intro-big-bg.png)] bg-cover"
>
	<Nav />
	<ScrollArrow position="right" />
	<div class="flex h-full flex-col items-center justify-center text-white">
		<h1 class="font-inter">Protegé lo que más querés con</h1>
		<h1 class="font-gabarito text-6xl font-extrabold uppercase">Titanio</h1>
	</div>
</section>
