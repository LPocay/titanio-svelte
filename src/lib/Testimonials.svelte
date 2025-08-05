<script>
	import LinkButton from './LinkButton.svelte';
	import ScrollArrow from './ScrollArrow.svelte';
</script>

<section
	class="relative flex h-screen w-full flex-col items-center justify-center bg-[url(/img/product-bg.png)] bg-cover text-white md:flex-row md:bg-[url(/img/product-big-bg.png)] md:pr-14 md:pl-40"
>
	<div class="mb-16 flex w-full flex-col items-start justify-center px-8">
		<div class="mb-4">
			<h1 class="text-xs md:text-[16px]">Testimonios</h1>
			<p class="text-2xl md:text-3xl">Lo que dicen nuestros clientes</p>
		</div>
		<LinkButton href="/history#tesimonials">Ver todos</LinkButton>
	</div>
	<div class="flex w-full flex-col items-center justify-center px-8 md:max-w-[42vw]">
		<ul class="w-full">
			<li
				class="border-b-solid testimonial overflow-hidden border-b border-b-white py-6 text-xl md:text-2xl"
			>
				<p class="testimonial-text overflow-hidden text-ellipsis whitespace-nowrap">
					"Esto es un testimonio de un cliente muy satisfecho con el producto 1"
				</p>
			</li>
			<li
				class="border-b-solid testimonial overflow-hidden border-b border-b-white py-6 text-xl md:text-4xl"
			>
				<p class="testimonial-text overflow-hidden text-ellipsis whitespace-nowrap">
					"Esto es un testimonio de un cliente muy satisfecho con el producto 1"
				</p>
			</li>
			<li
				class="border-b-solid testimonial overflow-hidden border-b border-b-white py-6 text-xl md:text-3xl"
			>
				<p class="testimonial-text overflow-hidden text-ellipsis whitespace-nowrap">
					"Esto es un testimonio de un cliente muy satisfecho con el producto 1"
				</p>
			</li>
			<li
				class="border-b-solid testimonial overflow-hidden border-b border-b-white py-6 text-xl md:text-2xl"
			>
				<p class="testimonial-text overflow-hidden text-ellipsis whitespace-nowrap">
					"Esto es un testimonio de un cliente muy satisfecho con el producto 1"
				</p>
			</li>
		</ul>
	</div>
	<ScrollArrow position="left" />
</section>

<style>
	.testimonial .testimonial-text {
		animation-play-state: paused;
	}

	.testimonial:hover .testimonial-text {
		text-overflow: unset;
		overflow: unset;
		animation: scroll-text 15s linear infinite;
		animation-play-state: running;
	}

	@keyframes scroll-text {
		from {
			transform: translateX(0%);
		}
		to {
			transform: translateX(-100%);
		}
	}
</style>
