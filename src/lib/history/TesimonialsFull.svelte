<script>
	import { browser } from '$app/environment';
	import { page } from '$app/state';
	import { onMount } from 'svelte';
	import ScrollArrow from '../ScrollArrow.svelte';

	if (browser) {
		onMount(() => {
			const hash = page.url.hash;
			if (hash) {
				const el = document.querySelector(hash);
				if (el) {
					setTimeout(() => {
						el.scrollIntoView({ behavior: 'smooth' });
					}, 200);
				}
			}
		});
	}
</script>

<section
	class="relative flex h-screen w-full flex-col items-center justify-center bg-[url(/img/product-bg.png)] bg-cover text-white md:bg-[url(/img/product-big-bg.png)] md:pr-14 md:pl-32"
	id="tesimonials"
>
	<div class="mb-12 flex w-full flex-col items-start justify-center px-8 md:px-0">
		<div class="mb-4">
			<h1 class="text-xs md:text-[16px]">Testimonios</h1>
			<p class="text-2xl md:text-3xl">Lo que dicen nuestros clientes</p>
		</div>
	</div>
	<div class="flex w-full flex-col items-center justify-center px-8 md:px-0">
		<ul class="flex w-full flex-col gap-8">
			<li class="border-b-solid overflow-hidden border-b border-b-white py-6 md:text-2xl">
				<p class="">"Esto es un testimonio de un cliente muy satisfecho con el producto 1"</p>
			</li>
			<li class="border-b-solid overflow-hidden border-b border-b-white py-6 text-xl md:text-4xl">
				<p class="">"Esto es un testimonio de un cliente muy satisfecho con el producto 1"</p>
			</li>
			<li class="border-b-solid overflow-hidden border-b border-b-white py-6 text-2xl md:text-3xl">
				<p class="">"Esto es un testimonio de un cliente muy satisfecho con el producto 1"</p>
			</li>
			<li class="border-b-solid overflow-hidden border-b border-b-white py-6 md:text-2xl">
				<p class="">"Esto es un testimonio de un cliente muy satisfecho con el producto 1"</p>
			</li>
		</ul>
	</div>
	<div class="max-sm:hidden">
		<ScrollArrow position="left" />
	</div>
</section>
