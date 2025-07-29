<script>
	import LinkButton from './LinkButton.svelte';
	import ScrollArrow from './ScrollArrow.svelte';
</script>

<section class="grid h-screen w-screen grid-rows-2 text-titanio-500">
	<div
		class="flex w-full flex-col items-start justify-end bg-[url(/img/story-bg.png)] px-10 pb-15 md:px-[15vw]"
	>
		<div class="mb-4">
			<h1 class="text-xs md:text-[16px]">Nuestra historia</h1>
			<p class="text-2xl md:text-3xl">
				Más de 70 años en el mercado brindando el mejor producto para tu seguridad.
			</p>
		</div>
		<LinkButton href="">Ver detalles</LinkButton>
	</div>
	<div>
	</div>
	<ScrollArrow position="left" />
</section>
