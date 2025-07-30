<script>
	import Carousel from './Carousel.svelte';
	import LinkButton from './LinkButton.svelte';
	import ScrollArrow from './ScrollArrow.svelte';
</script>

<section class="relative grid h-screen w-full grid-rows-2 text-titanio-500" id="historia">
	<div
		class="relative flex w-full flex-col items-start justify-end bg-[url(/img/story-bg.png)] px-10 pb-15 md:px-[15vw]"
	>
		<div class="mb-4">
			<h1 class="text-xs md:text-[16px]">Nuestra historia</h1>
			<p class="text-2xl md:text-3xl">
				Más de 70 años en el mercado brindando el mejor producto para tu seguridad.
			</p>
		</div>
		<LinkButton dark href="">Ver detalles</LinkButton>
		<div class="max-sm:hidden">
			<ScrollArrow dark position="right" />
		</div>
	</div>
	<div>
  <Carousel />
  </div>
	<div class="md:hidden">
		<ScrollArrow dark position="right" />
	</div>
</section>
