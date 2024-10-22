<script lang="ts">
  import GameOfLife from '$lib/GameOfLife.svelte';
</script>

<svelte:head>
  <title>Brian Pistar - Software Engineer & Web Developer</title>
</svelte:head>

<GameOfLife />

<div class="hero min-h-screen relative overflow-hidden bg-base-100 bg-opacity-80">
  <div class="hero-content text-center relative z-10">
    <div class="max-w-md">
      <h1 class="text-5xl font-bold">Brian Pistar</h1>
      <p class="py-6">Software Engineer & Web Developer</p>
      <a href="/projects" class="btn btn-primary">View My Work</a>
    </div>
  </div>
</div>

<div class="bg-base-300 bg-opacity-80 py-16">
  <div class="container mx-auto px-4">
    <h2 class="text-3xl font-bold mb-8 text-center">About Me</h2>
    <div class="grid md:grid-cols-2 gap-8 items-center">
      <div>
        <p class="mb-4">Hi, I'm Brian Pistar, a passionate software engineer specializing in web development. Self taught, and addicted to information.</p>
        <p>My passions include:</p>
        <ul class="list-disc list-inside mb-4">
          <li>Front-end: React, NextJS, Svelte</li>
          <li>Back-end: Node.js, Golang, Rust</li>
          <li>Blockchain: EVM smart contracts, and UI to interact with them</li>
        </ul>
        <a href="/about" class="btn btn-outline">Learn More About Me</a>
      </div>
      <div class="flex justify-center">
        <div class="avatar">
          <div class="w-64 rounded-full ring ring-secondary ring-offset-base-100 ring-offset-2">
            <img src="/images/profile.jpg" alt="Brian Pistar" />
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- <div class="bg-base-200 bg-opacity-80 py-16">
  <div class="container mx-auto px-4">
    <h2 class="text-3xl font-bold mb-8 text-center">Featured Projects</h2>
    <div class="grid md:grid-cols-3 gap-6">
      <div class="card bg-base-100 shadow-xl">
        <div class="card-body">
          <h3 class="card-title">Project 1</h3>
          <p>Brief description of Project 1</p>
          <div class="card-actions justify-end">
            <a href="/projects/project1" class="btn btn-primary btn-sm">View Details</a>
          </div>
        </div>
      </div>
      <div class="card bg-base-100 shadow-xl">
        <div class="card-body">
          <h3 class="card-title">Project 2</h3>
          <p>Brief description of Project 2</p>
          <div class="card-actions justify-end">
            <a href="/projects/project2" class="btn btn-primary btn-sm">View Details</a>
          </div>
        </div>
      </div>
      <div class="card bg-base-100 shadow-xl">
        <div class="card-body">
          <h3 class="card-title">Project 3</h3>
          <p>Brief description of Project 3</p>
          <div class="card-actions justify-end">
            <a href="/projects/project3" class="btn btn-primary btn-sm">View Details</a>
          </div>
        </div>
      </div>
    </div>
    <div class="text-center mt-8">
      <a href="/projects" class="btn btn-outline">View All Projects</a>
    </div>
  </div>
</div> -->

<div class="container mx-auto px-4 py-16">
  <h2 class="text-3xl font-bold mb-8 text-center">Get In Touch</h2>
  <div class="text-center">
    <p class="mb-4">Interested in working together or have any questions?</p>
    <a href="/contact" class="btn btn-primary">Contact Me</a>
  </div>
</div>
