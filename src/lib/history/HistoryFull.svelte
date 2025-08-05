<script lang="ts">
	import ScrollArrow from '../ScrollArrow.svelte';
</script>

<section
	class="relative flex h-screen w-full flex-col bg-[url(/img/product-bg.png)] bg-cover px-8 pt-16 pb-8 font-inter text-white md:flex-row md:items-center md:justify-between md:bg-[url(/img/product-big-bg.png)] md:p-0"
	id="producto"
>
	<ScrollArrow position="left" />
	<div
		class="md:flex md:w-full md:basis-[61%] md:flex-col md:items-start md:justify-center md:px-[15vw]"
	>
		<div class="mb-4">
			<p class="text-xl md:text-3xl">
				Acá va un texto resumido de la historia. Tiene que contar de donde nace el producto, el
				interés por la seguridad, y muchas cosas referentes a lo que se quiere exponer con las
				noticias. Debería ocupar estos renglones, asi nos queda bien la disposición.
			</p>
		</div>
	</div>
	<div
		class="mx-auto mt-4 h-full w-full max-w-[230px] rounded-[120px] bg-[url(https://placehold.co/600x400)] bg-center md:hidden"
	></div>
	<div class="h-full basis-[40%] bg-[url(https://placehold.co/600x400)] max-sm:hidden"></div>
</section>
