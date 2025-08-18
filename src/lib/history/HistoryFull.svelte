<script lang="ts">
	import Carousel from '$lib/Carousel.svelte';
	import ScrollArrow from '../ScrollArrow.svelte';

	const images = ['/img/sp1.png', '/img/sp2.png', '/img/sp3.png'];
</script>

<section
	class="relative z-[-2] flex h-screen w-full flex-col bg-[url(/img/product-bg.png)] bg-cover px-8 pt-16 pb-8 font-inter text-white md:flex-row md:items-center md:justify-between md:bg-[url(/img/product-big-bg.png)] md:p-0"
	id="producto"
>
	<ScrollArrow position="left" />
	<div
		class="md:flex md:w-full md:basis-[61%] md:flex-col md:items-start md:justify-center md:px-[15vw]"
	>
		<div class="mb-4">
			<p class="text-xl md:text-3xl">
				Desde una pequeña cerrajería nacida en Montserrat hace más de 50 años hasta el presente, nos
				apasiona lo mismo: la seguridad.
			</p>
		</div>
	</div>
	<div class="mx-auto mt-4 h-full w-full max-w-[230px] rounded-[120px] bg-center md:hidden">
		<Carousel auto {images} rounded />
	</div>
	<div class="h-full basis-[40%] max-sm:hidden">
		<Carousel auto {images} />
	</div>
</section>
