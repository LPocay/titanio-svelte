<script lang="ts">
	import slideButtonImg from '$lib/assets/slide-button.png';
	import { browser } from '$app/environment';
	import { onMount } from 'svelte';
	let {
		auto = false,
		images = [],
		rounded = false
	} = $props<{ auto?: boolean; images: string[]; rounded?: boolean }>();
	let isTransitioning = $state(false);
	let currentIndex = $state(0);
	let nextIndex = $state(0);
	let currentImgClasses = $state([
		'h-full',
		'w-full',
		'shrink-0',
		'basis-full',
		'object-cover',
		'absolute'
	]);
	let nextImgClasses = $state([
		'h-full',
		'w-full',
		'shrink-0',
		'basis-full',
		'object-cover',
		'absolute'
	]);

	if (browser) {
		onMount(() => {
			let interval: number;
			if (auto) {
				interval = setInterval(() => {
					nextImage();
				}, 2000);
			}
			return () => {
				clearInterval(interval);
			};
		});
	}

	function nextImage() {
		if (isTransitioning) return;
		isTransitioning = true;

		nextIndex = (currentIndex + 1) % images.length;
		currentImgClasses = currentImgClasses.concat('slide-leave-to-left');
		nextImgClasses = nextImgClasses.concat('slide-enter-from-right');
	}
	function prevImage() {
		if (isTransitioning) return;
		isTransitioning = true;

		nextIndex = currentIndex === 0 ? images.length - 1 : currentIndex - 1;
		currentImgClasses = currentImgClasses.concat('slide-leave-to-right');
		nextImgClasses = nextImgClasses.concat('slide-enter-from-left');
	}

	function onAnimationEnd() {
		currentImgClasses = currentImgClasses.slice(0, -1);
		nextImgClasses = nextImgClasses.slice(0, -1);
		isTransitioning = false;
		currentIndex = nextIndex;
	}
</script>

<div class="relative h-full w-full">
	<div class="absolute right-7 z-20 flex h-full items-center justify-center md:right-14">
		{#if !auto}
			<button class="cursor-pointer" onclick={nextImage}>
				<img src={slideButtonImg} alt="" />
			</button>
		{/if}
	</div>
	<div class="absolute left-7 z-20 flex h-full items-center justify-center md:left-14">
		{#if !auto}
			<button class="cursor-pointer" onclick={prevImage}>
				<img class="rotate-y-180" src={slideButtonImg} alt="" />
			</button>
		{/if}
	</div>
	<div class="shadow-x relative grid h-full w-full flex-nowrap overflow-hidden {rounded && "rounded-[120px]"}">
		<img
			class={currentImgClasses.join(' ')}
			style="z-index: -1;"
			src={images[currentIndex]}
			alt=""
			onanimationend={onAnimationEnd}
		/>
		{#if isTransitioning}
			<img style="z-index: -1;" class={nextImgClasses.join(' ')} src={images[nextIndex]} alt="" />
		{/if}
	</div>
</div>

<style>
	.slide-enter-from-right {
		animation-name: from-r-to-c;
		animation-duration: 300ms;
		animation-timing-function: ease-in-out;
		animation-fill-mode: forwards;
	}
	.slide-enter-from-left {
		animation-name: from-l-to-c;
		animation-duration: 300ms;
		animation-timing-function: ease-in-out;
		animation-fill-mode: forwards;
	}
	.slide-leave-to-left {
		animation-name: from-c-to-l;
		animation-duration: 300ms;
		animation-timing-function: ease-in-out;
		animation-fill-mode: forwards;
	}
	.slide-leave-to-right {
		animation-name: from-c-to-r;
		animation-duration: 300ms;
		animation-timing-function: ease-in-out;
		animation-fill-mode: forwards;
	}
	@keyframes from-r-to-c {
		from {
			transform: translateX(100%);
		}
		to {
			transform: translateX(0%);
		}
	}
	@keyframes from-l-to-c {
		from {
			transform: translateX(-100%);
		}
		to {
			transform: translateX(0%);
		}
	}
	@keyframes from-c-to-r {
		from {
			transform: translateX(0%);
		}
		to {
			transform: translateX(100%);
		}
	}
	@keyframes from-c-to-l {
		from {
			transform: translateX(0%);
		}
		to {
			transform: translateX(-100%);
		}
	}
	.shadow-x {
		box-shadow:
			72px 7px 101px -70px rgba(0, 0, 0, 0.75) inset,
			-72px 7px 101px -70px rgba(0, 0, 0, 0.75) inset;
	}
</style>
