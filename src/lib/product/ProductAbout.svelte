<script lang="ts">
	import LinkButton from '$lib/LinkButton.svelte';
	import ScrollArrow from '../ScrollArrow.svelte';
</script>

<section
	class="relative flex h-screen w-full flex-col bg-[url(/img/product-bg.png)] bg-cover px-8 pt-28 pb-8 font-inter text-white md:flex-row md:items-center md:justify-between md:bg-[url(/img/product-big-bg.png)] md:p-0"
	id="producto"
>
	<div class="md:hidden">
		<div class="mb-4">
			<h1 class="text-xs md:text-[16px]">El producto</h1>
			<p class="text-2xl md:text-3xl">
				Titanio es un barral para proteger tu hogar, a un precio accesible.
			</p>
		</div>
		<LinkButton href="">Ver especificaciones</LinkButton>
	</div>

	<div
		class="hide-scroll mx-[-2rem] mt-12 flex h-full gap-11 overflow-x-auto px-8 md:mx-0 md:mt-0 md:w-full md:justify-evenly"
	>
		<div class="flex h-full min-w-[198px] flex-col md:max-w-[336px] md:justify-center">
			<div
				class="h-full rounded-[120px] bg-[url(/img/p1.png)] bg-cover bg-center md:mx-auto md:max-h-[400px] md:min-w-[250px] max-sm:max-h-[338px]"
			></div>
			<div class="mt-3">
				<h2 class="text-xs md:text-[16px]">El barral</h2>
				<p class="md:text-[18px]">
					Sin requerir de una obra, este sistema único en el país, asegura tu hogar de la mejor
					manera.
				</p>
			</div>
		</div>
		<div
			class="flex h-full min-w-[198px] flex-col md:max-w-[336px] md:translate-y-[-53px] md:justify-center"
		>
			<div
				class="h-full rounded-[120px] bg-[url(/img/p2.png)] bg-cover bg-center md:mx-auto md:max-h-[400px] md:min-w-[250px]"
			></div>
			<div class="mt-3">
				<h2 class="text-xs md:text-[16px]">La colocación</h2>
				<p class="md:text-[18px]">
					Nuestro sistema de anclaje de orejas y espiga de acero se fija independiente al marco,
					generando una resistencia única en el mercado.
				</p>
			</div>
		</div>
		<div class="flex h-full min-w-[198px] flex-col md:max-w-[336px] md:justify-center">
			<div
				class="h-full rounded-[120px] bg-[url(/img/p3.png)] bg-cover bg-center md:mx-auto md:max-h-[400px] md:min-w-[250px]"
			></div>
			<div class="mt-3">
				<h2 class="text-xs md:text-[16px]">El barral</h2>
				<p class="md:text-[18px]">
					Apertura con llave anti-ganzúa y protector de acero templado, sumado a un anti-pánico
					interior para una evacuación segura en caso de emergencias sin llaves.
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
