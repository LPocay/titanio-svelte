<script>
	import ScrollArrow from '../ScrollArrow.svelte';
</script>

<section class="relative md:grid md:h-screen w-full grid-rows-2 text-titanio-500" id="quality">
	<div
		class="relative flex w-full flex-col items-start justify-center bg-[url(/img/history-bg.png)] px-8 py-16 md:px-20 md:pb-11"
	>
		<div class="mb-4 md:max-w-[920px]">
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
	<div class="max-sm:hidden">
    <video src="/video/v2.mp4" autoplay muted loop class="w-full h-full object-cover"></video>
  </div>
</section>
