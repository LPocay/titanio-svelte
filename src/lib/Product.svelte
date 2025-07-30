<script lang="ts">
	import LinkButton from './LinkButton.svelte';
	import ScrollArrow from './ScrollArrow.svelte';
</script>

<section
	class="relative flex h-screen w-full flex-col bg-[url(/img/product-bg.png)] px-8 pt-28 pb-8 font-inter text-white md:flex-row md:items-center md:justify-between md:bg-[url(/img/product-big-bg.png)] bg-cover md:p-0"
	id="producto"
>
	<ScrollArrow position="left" />
	<div
		class="md:flex md:w-full md:basis-[61%] md:flex-col md:items-start md:justify-center md:px-[15vw]"
	>
		<div class="mb-4">
			<h1 class="text-xs md:text-[16px]">El producto</h1>
			<p class="text-2xl md:text-3xl">
				Titanio es un barral para proteger tu hogar, a un precio accesible.
			</p>
		</div>
		<LinkButton href="">Ver especificaciones</LinkButton>
	</div>
	<div
		class="mx-auto mt-16 h-full w-full max-w-[230px] rounded-[120px] bg-[url(https://placehold.co/600x400)] bg-center md:hidden"
	></div>
	<div class="h-full basis-[40%] bg-[url(https://placehold.co/600x400)] max-sm:hidden"></div>
</section>
