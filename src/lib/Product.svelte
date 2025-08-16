<script lang="ts">
	import LinkButton from './LinkButton.svelte';
	import ScrollArrow from './ScrollArrow.svelte';

	export function playOnView(
		node: HTMLVideoElement,
		opts: { threshold?: number; rootMargin?: string; resetOnLeave?: boolean } = {}
	) {
		const { threshold = 0.5, rootMargin = '150px 0px', resetOnLeave = false } = opts;

		node.muted = true;
		node.playsInline = true;

		let observer: IntersectionObserver | null = null;

		if (typeof IntersectionObserver !== 'undefined') {
			observer = new IntersectionObserver(
				async ([entry]) => {
					const visible = entry.isIntersecting && entry.intersectionRatio >= threshold;
					try {
						if (visible) {
							await node.play();
						} else {
							node.pause();
							if (resetOnLeave) node.currentTime = 0;
						}
					} catch {
						// silencioso: algunos navegadores pueden bloquear play() en casos raros
					}
				},
				{ threshold: [0, threshold, 1], rootMargin }
			);

			observer.observe(node);
		}

		return {
			destroy() {
				if (observer) observer.disconnect();
				node.pause();
			}
		};
	}
</script>

<section
	class="relative flex h-screen w-full flex-col bg-[url(/img/product-bg.png)] bg-cover px-8 pt-28 pb-8 font-inter text-white md:flex-row md:items-center md:justify-between md:bg-[url(/img/product-big-bg.png)] md:p-0"
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
		<LinkButton href="/product#producto">Ver especificaciones</LinkButton>
	</div>
	<div
		class="mx-auto mt-16 h-full w-full max-w-[230px] rounded-[120px] bg-[url(/img/barral-mobile.png)] bg-cover bg-center md:hidden"
	>
		<video
			src="/video/v1.mp4"
			autoplay
			muted
			loop
			class="h-full w-full rounded-[120px] object-cover"
			use:playOnView={{ threshold: 0.5, rootMargin: '150px 0px' }}
		></video>
	</div>
	<div class="h-full basis-[40%] bg-[url(/img/barral.png)] bg-cover max-sm:hidden">
		<video
			src="/video/v1.mp4"
			preload="metadata"
			playsinline
			muted
			loop
			class="h-full w-full object-none"
			use:playOnView={{ threshold: 0.5, rootMargin: '150px 0px' }}
		></video>
	</div>
</section>
