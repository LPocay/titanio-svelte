<script>
	import LinkButton from './LinkButton.svelte';
	import ScrollArrow from './ScrollArrow.svelte';
	const testimonials = [
		'Esto es un testimonio de un cliente muy satisfecho con el producto 1',
		'Esto es un testimonio de un cliente muy satisfecho con el producto 2',
		'Esto es un testimonio de un cliente muy satisfecho con el producto 3',
		'Esto es un testimonio de un cliente muy satisfecho con el producto 4'
	];
</script>

<section
	class="flex h-screen w-full flex-col items-center justify-center bg-[url(/img/product-bg.png)] bg-cover text-white md:flex-row md:bg-[url(/img/product-big-bg.png)] md:pl-40 md:pr-14"
>
	<div class="mb-16 flex w-full flex-col items-start justify-center px-8">
		<div class="mb-4">
			<h1 class="text-xs md:text-[16px]">Testimonios</h1>
			<p class="text-2xl md:text-3xl">Lo que dicen nuestros clientes</p>
		</div>
		<LinkButton href="">Ver todos</LinkButton>
	</div>
	<div class="flex w-full flex-col items-center justify-center px-8 max-w-[42vw]">
		<ul class="w-full">
			{#each testimonials as tesmonie (tesmonie)}
				<li class="border-b-solid border-b border-b-white py-6 text-xl md:text-2xl">
					<p class="overflow-hidden text-ellipsis whitespace-nowrap">
						"{tesmonie}"
					</p>
				</li>
			{/each}
		</ul>
	</div>
	<ScrollArrow position="left" />
</section>
