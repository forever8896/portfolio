<script lang="ts">
  import GameOfLife from '$lib/GameOfLife.svelte';
  import { fade, fly, scale, slide } from 'svelte/transition';
  import { elasticOut } from 'svelte/easing';
  import { onMount } from 'svelte';

  let visible = false;
  let aboutVisible = false;
  let contactVisible = false;
  let listVisible = false;

  onMount(() => {
    visible = true;
  });

  function intersectionObserver(node: HTMLElement, callback: IntersectionObserverCallback) {
    const observer = new IntersectionObserver(callback, {
      rootMargin: '0px',
      threshold: 0.1
    });

    observer.observe(node);

    return {
      destroy() {
        observer.unobserve(node);
      }
    };
  }

  function handleIntersection(entries: IntersectionObserverEntry[]) {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        if (entry.target.id === 'about') aboutVisible = true;
        if (entry.target.id === 'contact') contactVisible = true;
        if (entry.target.id === 'about-list') listVisible = true;
      }
    });
  }

  let avatarVisible = false;

  function showAvatar() {
    setTimeout(() => avatarVisible = true, 500);
  }

  function sequentialFly(node: HTMLElement, { delay = 0, duration = 500 }) {
    return {
      delay,
      duration,
      css: (t: number) => {
        const eased = elasticOut(t);
        return `
          opacity: ${t};
          transform: translateY(${(1 - eased) * 20}px);
        `;
      }
    };
  }

  const passions = [
    'Front-end: React, NextJS, Svelte',
    'Back-end: Golang, Rust',
    'Blockchain: EVM smart contracts, and UI to interact with them'
  ];

  $: if (aboutVisible) {
    setTimeout(() => {
      listVisible = true;
    }, 800); // Delay the list appearance
  }
</script>

<svelte:head>
  <title>Brian Pistar - Software Engineer & Web Developer</title>
</svelte:head>

<GameOfLife />

{#if visible}
  <div transition:fade={{ duration: 1000 }} class="hero min-h-screen relative overflow-hidden bg-base-100 bg-opacity-80">
    <div class="hero-content text-center relative z-10">
      <div class="max-w-md">
        <h1 transition:fly={{ y: -50, duration: 1000 }} class="text-5xl font-bold">Brian Pistar</h1>
        <p transition:fly={{ y: 50, duration: 1000, delay: 500 }} class="py-6">Software Engineer & Web Developer</p>
      </div>
    </div>
  </div>

  <div 
    id="about"
    use:intersectionObserver={handleIntersection}
    class="bg-base-300 bg-opacity-80 py-16"
  >
    {#if aboutVisible}
      <div class="container mx-auto px-4">
        <h2 in:fly={{ y: 20, duration: 500, delay: 200 }} class="text-3xl font-bold mb-8 text-center">About Me</h2>
        <div class="grid md:grid-cols-2 gap-8 items-start">
          <div class="min-h-[400px]">
            <p in:fly={{ y: 20, duration: 500, delay: 400 }} class="mb-4">Hi, I'm Brian Pistar, a passionate software engineer specializing in web development. Self taught, and addicted to information.</p>
            <p in:fly={{ y: 20, duration: 500, delay: 600 }} class="mb-4">My passions include:</p>
            <ul in:fly={{ y: 20, duration: 500, delay: 800 }} class="list-disc list-inside mb-4">
              {#each passions as passion}
                <li>{passion}</li>
              {/each}
            </ul>
            <a in:fly={{ y: 20, duration: 500, delay: 1000 }} href="/about" class="btn btn-outline">Learn More About Me</a>
          </div>
          <div class="flex justify-center">
            {#if avatarVisible}
              <div 
                in:fade={{ duration: 500, delay: 400 }}
                class="avatar"
              >
                <div class="w-64 rounded-full ring ring-secondary ring-offset-base-100 ring-offset-2 shadow-lg">
                  <img src="/images/profile.jpg" alt="Brian Pistar" />
                </div>
              </div>
            {/if}
          </div>
        </div>
      </div>
    {/if}
  </div>

  <div 
    id="contact"
    use:intersectionObserver={handleIntersection}
    class="container mx-auto px-4 py-16"
  >
    {#if contactVisible}
      <div in:fade={{ duration: 1000 }}>
        <h2 class="text-3xl font-bold mb-8 text-center">Get In Touch</h2>
        <div class="text-center">
          <p class="mb-4">Interested in working together or have any questions?</p>
          <a href="/contact" class="btn btn-primary">Contact Me</a>
        </div>
      </div>
    {/if}
  </div>
{/if}

{#if aboutVisible}
  {showAvatar()}
{/if}
