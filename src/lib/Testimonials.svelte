<script>
	import LinkButton from './LinkButton.svelte';
	import ScrollArrow from './ScrollArrow.svelte';
	import startSVG from '$lib/assets/star.svg';
</script>

<section
	class="relative flex h-screen w-full flex-col items-center justify-center bg-[url(/img/product-bg.png)] bg-cover text-white md:flex-row md:bg-[url(/img/product-big-bg.png)] md:pr-14 md:pl-40"
>
	<div class="mb-16 flex w-full flex-col items-start justify-center px-8">
		<div class="mb-4">
			<h1 class="text-xs md:text-[16px]">Testimonios</h1>
			<p class="text-2xl md:text-3xl">Lo que dicen nuestros clientes</p>
			<div class="max-sm:hidden flex gap-1.5 mt-4">
				<img src={startSVG} alt="" />
				<img src={startSVG} alt="" />
				<img src={startSVG} alt="" />
				<img src={startSVG} alt="" />
				<img src={startSVG} alt="" />
			</div>
		</div>
		<LinkButton target="#testimonials" href="/history">Ver todos</LinkButton>
	</div>
	<div class="flex w-full flex-col items-center justify-center px-8 md:max-w-[42vw]">
		<ul class="w-full">
			<li
				class="border-b-solid testimonial overflow-hidden border-b border-b-white py-6 text-xl md:text-2xl"
			>
				<p class="testimonial-text overflow-hidden text-ellipsis whitespace-nowrap">
					“Realicé un blindaje bunker, retiraron mi puerta, colocaron una provisoria y, en el plazo
					pactado, instalaron la nueva con una prolijidad sobresaliente. Encajó a la perfección y al
					cerrarla se siente segura como una bóveda de banco. Trabajan de forma impecable, y algo
					muy importante, con un precio más que justificado., realmente sentís que pagaste por un
					producto que está a la altura. Altamente recomendable: los volvería a contratar sin
					dudarlo.”
				</p>
			</li>
			<li
				class="border-b-solid testimonial overflow-hidden border-b border-b-white py-6 text-xl md:text-4xl"
			>
				<p class="testimonial-text overflow-hidden text-ellipsis whitespace-nowrap">
					“Los llamé por un trabajo que era bastante difícil, una puerta que da directo a la calle,
					de mas de 3 metros de altura, nunca había hecho hacer el trabajo por que los precios que
					me habían pasado eran precios que se iban completamente de mi presupuesto y del de varios
					jaja, Ellos vinieron, me pasaron un precio que si bien me aclararon era mas alto que el de
					una puerta normal, no era impagable, lo realizaron aquí mismo en el día y el resultado fue
					impecable, los recomiendo 100%, ahora estoy tranquilo!”
				</p>
			</li>
			<li
				class="border-b-solid testimonial overflow-hidden border-b border-b-white py-6 text-xl md:text-3xl"
			>
				<p class="testimonial-text overflow-hidden text-ellipsis whitespace-nowrap">
					“Me los recomendó un amigo en común, el cual es amigo personal de Javier Gutierrez, no
					blindé las puertas por que me dijeron que al ser puertas de chapa no había necesidad del
					gasto en blindaje, instalaron los barrales titanio en media mañana, limpiaron todo y quedó
					todo prolijo, la verdad, se nota que hace mucho que hacen esto, rápido, limpio y claros,
					ya se los recomendé a varios amigos y conocidos.”
				</p>
			</li>
			<li
				class="border-b-solid testimonial overflow-hidden border-b border-b-white py-6 text-xl md:text-2xl"
			>
				<p class="testimonial-text overflow-hidden text-ellipsis whitespace-nowrap">
					“Por razones de seguridad prefiero no dar mis datos, pero instalé los barrales, en una
					zona rural, en la cual ya había probado de todo y como no suelo ir salvo fines de semana,
					siempre me encontraba con mi casa desvalijada, ya en un momento dejé de reponer las cosas
					que me llevaban, cuando encontré este sistema en internet y vi el video, me tiré el lance.
					Fue la mejor decisión que tomé, intentaron abrir mi puerta durante horas y finalmente
					desistieron, probaron de todo y el barral nunca cedió, gracias al servicio que ofrecen y
					la atención de Javier y de Luis, que siempre estuvieron atentos a cualquier duda, y que
					después de que intentaron abrir mi puerta vinieron y revisaron que todo esté bien, mi
					agradecimiento y recomendación para ellos.”
				</p>
			</li>
		</ul>
	</div>
	<ScrollArrow position="left" />
</section>

<style>
	.testimonial .testimonial-text {
		animation-play-state: paused;
	}

	.testimonial:hover .testimonial-text {
		text-overflow: unset;
		overflow: unset;
		animation: scroll-text 15s linear infinite;
		animation-play-state: running;
	}

	@keyframes scroll-text {
		from {
			transform: translateX(0%);
		}
		to {
			transform: translateX(-100%);
		}
	}
</style>
