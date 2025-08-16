<script lang="ts">
	import ScrollArrow from '../ScrollArrow.svelte';
</script>

<section
	class="relative flex h-screen w-full flex-col bg-[url(/img/history-bg.png)] bg-cover px-8 pt-16 pb-16 font-inter text-white md:flex-row md:items-center md:justify-between md:bg-[url(/img/history-big-bg.png)] md:p-0"
	id="producto"
>
	<div class="max-sm:hidden">
		<ScrollArrow dark position="right" />
	</div>
	<div
		class="text-titanio-500 md:flex md:w-full md:basis-[61%] md:flex-col md:items-start md:justify-center md:px-[8vw]"
	>
		<div class="mb-4">
			<p class="mb-4 italic md:mb-4 md:text-3xl font-inter font-light">
				“Con más de 50 años dedicados al desarrollo de tecnologias en materia de seguridad, TITANIO
				nació fruto de la necesidad de un producto de alta resistencia contra entraderas. Hoy con
				orgullo, aseguramos que es el único producto de su tipo en Argentina, garantizando la
				seguridad del cliente.”
			</p>
			<p class="text-xl font-semibold md:text-3xl">Javier Gutierrez, Co-Founder</p>
		</div>
	</div>
	<div
		class="mx-auto mt-4 h-full w-full max-w-[233px] rounded-[120px] bg-[url(/img/ceo.png)] bg-cover bg-center md:max-h-[450px] md:max-w-[300px] md:rounded-[180px]"
	></div>
</section>
