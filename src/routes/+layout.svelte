<script lang="ts">
	import '../app.css';
	import { onMount } from 'svelte';
	import { writable, type Writable } from 'svelte/store';
	import { slide, fade } from 'svelte/transition';

	const isMenuOpen: Writable<boolean> = writable(false);
	const isNavVisible: Writable<boolean> = writable(false);

	let innerWidth: number;
	let lastScrollY = 0;

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
  <nav class="bg-primary text-base-200 p-4 fixed w-full z-50 transition-transform duration-300"
       class:translate-y-0={$isNavVisible} class:-translate-y-full={!$isNavVisible}>
    <div class="container mx-auto flex justify-between items-center">
      <a href="/" class="btn btn-ghost hover:text-white text-xl">Home</a>
      <button class="md:hidden btn btn-ghost" on:click={toggleMenu} aria-label="Menu">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" class="w-6 h-6">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7" />
        </svg>
      </button>
      <div class="hidden md:flex space-x-4">
        <a href="/projects" class="btn btn-ghost hover:text-white text-xl">Projects</a>
        <a href="/about" class="btn btn-ghost hover:text-white text-xl">About</a>
        <a href="/blog" class="btn btn-ghost hover:text-white text-xl">Blog</a>
        <a href="/contact" class="btn btn-ghost hover:text-white text-xl">Contact</a>
      </div>
    </div>
  </nav>

  {#if $isMenuOpen && innerWidth <= 768}
    <div transition:fade={{ duration: 300 }} class="fixed inset-0 bg-primary text-base-200 z-50 overflow-y-auto">
      <div class="flex justify-end p-4">
        <button on:click={closeMenu} class="btn btn-ghost text-xl" aria-label="Close menu">
          &times;
        </button>
      </div>
      <div class="flex flex-col items-center space-y-4 mt-16">
        <a href="/projects" class="btn btn-ghost hover:bg-primary-focus text-xl w-full" on:click={closeMenu}>Projects</a>
        <a href="/about" class="btn btn-ghost hover:bg-primary-focus text-xl w-full" on:click={closeMenu}>About</a>
        <a href="/blog" class="btn btn-ghost hover:bg-primary-focus text-xl w-full" on:click={closeMenu}>Blog</a>
        <a href="/contact" class="btn btn-ghost hover:bg-primary-focus text-xl w-full" on:click={closeMenu}>Contact</a>
      </div>
    </div>
  {/if}
  
  <main class="flex-grow container mx-auto p-4 mt-16">
    <slot />
  </main>
  
  <footer class="bg-base-200 p-4 text-center">
    <p>&copy; 2024 Brian Pistar. All rights reserved.</p>
  </footer>
</div>
