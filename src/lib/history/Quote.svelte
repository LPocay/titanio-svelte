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
		class="text-titanio-500 md:flex md:w-full md:basis-[61%] md:flex-col md:items-start md:justify-center md:px-[10vw]"
	>
		<div class="mb-4">
			<p class="text-2xl italic md:text-3xl md:mb-4">
				“Acá me gustaría que pongamos una cita de algo que represente para vos que significa
				titanio, por qué es algo que te apasiona.”
			</p>
			<p class="text-xl font-semibold md:text-3xl">Javier Gutierrez, Co-Founder</p>
		</div>
	</div>
	<div
		class="mx-auto mt-4 h-full w-full max-w-[233px] rounded-[120px] bg-[url(https://placehold.co/600x400/black/white)] bg-center md:max-w-[300px] md:max-h-[450px] md:rounded-[180px]"
	></div>
</section>
