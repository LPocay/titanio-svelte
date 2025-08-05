<script lang="ts">
	import { page } from '$app/state';
	import closeButtonImg from '$lib/assets/close.svg';

	let isOpen = $state(false);
	function closeMenu() {
		isOpen = false;
	}
	function openMenu() {
		isOpen = true;
	}
	function getContactHref() {
		if (page.url.pathname === '/') {
			return '#charlemos';
		}

		return '/#charlemos';
	}
</script>

<nav class="absolute z-10 flex w-full justify-between p-8 font-inter text-white md:p-14">
	<a href="/">
		<img src="/img/logo.svg" alt="" />
	</a>
	<ul class="grid grid-cols-3 gap-72 text-xl max-sm:hidden">
		<li>
			<a class={page.url.pathname === '/product' ? 'underline' : ''} href="/product">Producto</a>
		</li>
		<li>
			<a class={page.url.pathname === '/history' ? 'underline' : ''} href="history">Historia</a>
		</li>
		<li>
			<a href={getContactHref()}>Charlemos</a>
		</li>
	</ul>
	<button class="cursor-pointer md:hidden" onclick={openMenu}>
		<img src="/img/bread.svg" alt="" />
	</button>
	<div
		class="fixed top-0 left-0 z-50 flex h-screen w-screen flex-col bg-titanio-500 p-8 md:hidden {isOpen
			? 'show-m'
			: 'close'}"
	>
		<button class="mb-16 ml-auto cursor-pointer" onclick={closeMenu}>
			<img src={closeButtonImg} alt="" />
		</button>
		<ul class="flex flex-col gap-4 text-xl">
			<li>
				<a href="/product">Producto</a>
			</li>
			<li>
				<a href="history">Historia</a>
			</li>
			<li>
				<a onclick={closeMenu} href={getContactHref()}>Charlemos</a>
			</li>
		</ul>
	</div>
</nav>

<style>
	.close {
		animation: close-menu 200ms ease-in-out forwards;
	}
	.show-m {
		animation: show-menu 200ms ease-in-out forwards;
	}
	@keyframes show-menu {
		from {
			transform: translateX(100%);
		}
		to {
			transform: translateX(0%);
		}
	}
	@keyframes close-menu {
		from {
			transform: translateX(0%);
		}
		to {
			transform: translateX(100%);
		}
	}
</style>
