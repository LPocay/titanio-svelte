<script lang="ts">
	import LinkButton from '$lib/LinkButton.svelte';
	import ScrollArrow from '../ScrollArrow.svelte';
</script>

<section
	class="relative flex h-screen w-full flex-col bg-[url(/img/product-bg.png)] bg-cover px-8 pt-28 pb-8 font-inter text-white md:flex-row md:items-center md:justify-between md:bg-[url(/img/product-big-bg.png)] md:p-0"
	id="producto"
>
	<div class="mb-4">
		<h1 class="text-xs md:text-[16px]">El producto</h1>
		<p class="text-2xl md:text-3xl">
			Titanio es un barral para proteger tu hogar, a un precio accesible.
		</p>
	</div>
	<LinkButton href="">Ver especificaciones</LinkButton>

	<div class="hide-scroll mx-[-2rem] mt-12 flex h-full gap-11 overflow-x-auto px-8">
		<div class="flex h-full min-w-[198px] flex-col">
			<div class="h-full rounded-[120px] bg-[url(https://placehold.co/600x400)]"></div>
			<div class="mt-3">
				<h2 class="text-xs md:text-[16px]">El barral</h2>
				<p class="md:text-3xl">
					Titanio es un barral para proteger tu hogar, a un precio accesible.
				</p>
			</div>
		</div>
		<div class="flex h-full min-w-[198px] flex-col">
			<div class="h-full rounded-[120px] bg-[url(https://placehold.co/600x400)]"></div>
			<div class="mt-3">
				<h2 class="text-xs md:text-[16px]">El barral</h2>
				<p class="md:text-3xl">
					Titanio es un barral para proteger tu hogar, a un precio accesible.
				</p>
			</div>
		</div>
		<div class="flex h-full min-w-[198px] flex-col">
			<div class="h-full rounded-[120px] bg-[url(https://placehold.co/600x400)]"></div>
			<div class="mt-3">
				<h2 class="text-xs md:text-[16px]">El barral</h2>
				<p class="md:text-3xl">
					Titanio es un barral para proteger tu hogar, a un precio accesible.
				</p>
			</div>
		</div>
	</div>
	<div class="max-sm:hidden">
		<ScrollArrow position="left" />
	</div>
</section>

<style>
	.hide-scroll::-webkit-scrollbar {
		display: none;
	}

	.hide-scroll {
		-ms-overflow-style: none; /* IE and Edge */
		scrollbar-width: none; /* Firefox */
	}
</style>
