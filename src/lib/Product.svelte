<script lang="ts">
	import LinkButton from './LinkButton.svelte';
	import ScrollArrow from './ScrollArrow.svelte';
</script>

<section
	class="relative h-screen w-screen bg-[url(/img/product-bg.png)] px-8 pt-28 pb-8 font-inter text-white flex flex-col"
	id="producto"
>
	<ScrollArrow position="left" />
	<div class="mb-4">
		<h1 class="text-xs">El producto</h1>
		<p class="text-2xl">Titanio es un barral para proteger tu hogar, a un precio accesible.</p>
	</div>
	<LinkButton>Ver especificaciones</LinkButton>
  <div class="bg-[url(https://placehold.co/600x400)] h-full w-full max-w-[230px] mx-auto bg-center mt-16 rounded-[120px]"></div>
</section>
