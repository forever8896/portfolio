<script lang="ts">
	import '../app.css';
	import { onMount } from 'svelte';
	import { writable, type Writable } from 'svelte/store';
	import { slide, fade } from 'svelte/transition';
  import Navbar from '$lib/components/Navbar.svelte';
  import Footer from '$lib/components/Footer.svelte';

	const isMenuOpen: Writable<boolean> = writable(false);
	const isNavVisible: Writable<boolean> = writable(false);

	let innerWidth: number;
	let lastScrollY = 0;


  let currentYear = new Date().getFullYear();

	onMount(() => {
		const handleScroll = () => {
			const currentScrollY = window.scrollY;
			isNavVisible.set(currentScrollY < lastScrollY);
			lastScrollY = currentScrollY;
		};

		window.addEventListener('scroll', handleScroll, { passive: true });

		const unsubscribe = isMenuOpen.subscribe((value: boolean) => {
			if (innerWidth > 768 && value) {
				isMenuOpen.set(false);
			}
		});

		return () => {
			window.removeEventListener('scroll', handleScroll);
			unsubscribe();
		};
	});

	function toggleMenu(): void {
		isMenuOpen.update((value: boolean) => !value);
	}

	function closeMenu(): void {
		isMenuOpen.set(false);
	}
</script>

<svelte:window bind:innerWidth />

<style lang="postcss">
  :global(::-webkit-scrollbar) {
    width: 10px;
  }

  :global(::-webkit-scrollbar-track) {
    background: transparent;
  }

  :global(::-webkit-scrollbar-thumb) {
    background-color: #20bc54;
    border-radius: 5px;
  }

 

  /* For Firefox */
  :global(html) {
    scrollbar-width: thin;
    scrollbar-color: #20bc54 transparent;
  }

  :global(html:hover) {
    scrollbar-color: #1ba97d transparent;
  }
</style>

<div class="min-h-screen flex flex-col">
 <Navbar />
  
  <main class="flex-grow container mx-auto p-4 mt-16">
    <slot  />
  </main>
  
    <Footer {currentYear} />
</div>
