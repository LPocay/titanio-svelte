<script>
	import ScrollArrow from '../ScrollArrow.svelte';
</script>

<section class="relative grid h-screen w-full grid-rows-2 text-titanio-500" id="quality">
	<div
		class="relative flex w-full flex-col items-start justify-center bg-[url(/img/story-bg.png)] px-8 md:px-[15vw] md:justify-end md:pb-11"
	>
		<div class="mb-4">
			<h1 class="text-xs md:text-2xl">Calidad garantizada</h1>
			<p class="text-2xl md:text-4xl md:pr-44">
				El barral está testeado contra intentos de apertura de todo tipo, probando que es uno de los
				mejores productos en el mercado para cuidar tu hogar de manera accesible.
			</p>
		</div>
		<div class="max-sm:hidden">
			<ScrollArrow dark position="right" />
		</div>
	</div>
	<div></div>
</section>
