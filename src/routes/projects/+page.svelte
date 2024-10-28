<svelte:head>
  <title>Projects - Brian Pistar</title>
</svelte:head>

<script lang="ts">
  import { spring } from 'svelte/motion';
  import { fade } from 'svelte/transition';
  import { writable } from 'svelte/store';

  const projects = [
   
    {
      name: "Allstake",
      description: "Web3 platform utilizing Thirdweb, Moralis, NextJs.",
      link: "projects/allstake",
      image: "/images/projects/allstake.png",
      badges: ["Web3", "Thirdweb", "Moralis", "Next.js"]
    },
    {
      name: "Cellular Domination Station",
      description: "Game-of-life inspired game, built in 10 days for the Revival Game jam, using phaser and svelte.",
      link: "projects/cellular-domination-station",
      image: "/images/projects/cellular-domination-station.png",
      badges: ["Phaser", "Svelte", "Game Jam"]
    },
    {
      name: "MindFlow",
      description: "Simple private note taking and habit tracker.",
      link: "projects/mindflow",
      image: "/images/projects/mindflow.png",
      badges: ["Svelte", "Tauri", "Rust"]
    },
    {
      name: "CrypTick",
      description: "A crypto alert app built in rust, tauri and svelte.",
      link: "projects/cryptick",
      image: "/images/projects/cryptick.png",
      badges: ["Rust", "Tauri", "Svelte"]
    },
    {
      name: "Magees",
      description: "A store with herbal stimulants, utilizing stripe, nextjs.",
      link: "projects/magees",
      image: "/images/projects/magees.png",
      badges: ["Next.js", "Stripe", "E-commerce"]
    },
  ];

  const hoveredProject = writable(null);

  function handleMouseEnter(project: any) {
    hoveredProject.set(project);
  }

  function handleMouseLeave() {
    hoveredProject.set(null);
  }

  $: scale = spring(1);
  $: rotation = spring(0);

  $: if ($hoveredProject) {
    scale.set(1.05);
    rotation.set(2);
  } else {
    scale.set(1);
    rotation.set(0);
  }

  // Function to determine badge color
  function getBadgeColor(badge: string, index: number): string {
    const colors = ['primary', 'secondary', 'accent', 'info', 'success', 'warning', 'error'];
    
    // You can customize this logic based on your preferences
    if (badge.toLowerCase().includes('react') || badge.toLowerCase().includes('next.js')) {
      return 'badge-primary';
    } else if (badge.toLowerCase().includes('svelte')) {
      return 'badge-secondary';
    } else if (badge.toLowerCase().includes('rust') || badge.toLowerCase().includes('go')) {
      return 'badge-accent';
    } else if (badge.toLowerCase().includes('web3') || badge.toLowerCase().includes('crypto')) {
      return 'badge-info';
    } else {
      // If no specific match, cycle through colors based on index
      return `badge-${colors[index % colors.length]}`;
    }
  }
</script>

<style>
  .card {
    transition: all 0.3s ease;
  }
</style>

<div class="container mx-auto px-4 py-8" in:fade={{ duration: 300 }}>
  <h1 class="text-4xl font-bold mb-4">My Projects</h1>
  <p class="text-lg mb-8">Here are some of my recent projects:</p>

  <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
    {#each projects as project}
      <a 
        href={project.link} 
        class="card card-compact bg-base-200 shadow-xl overflow-hidden hover:shadow-2xl"
        on:mouseenter={() => handleMouseEnter(project)}
        on:mouseleave={handleMouseLeave}
        style="transform: scale({$hoveredProject === project ? $scale : 1}) rotate({$hoveredProject === project ? $rotation : 0}deg);"
      >
        <figure>
          <img src={project.image} alt={project.name} class="w-full h-48 object-cover" />
        </figure>
        <div class="card-body bg-black">
          <h2 class="card-title text-primary">{project.name}</h2>
          <p class="text-sm mb-4">{project.description}</p>
          <div class="card-actions justify-end">
            {#each project.badges as badge, index}
              <div class="badge badge-outline {getBadgeColor(badge, index)}">{badge}</div>
            {/each}
          </div>
        </div>
      </a>
    {/each}
  </div>
</div>
