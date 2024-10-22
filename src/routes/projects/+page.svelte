<svelte:head>
  <title>Projects - Brian Pistar</title>
</svelte:head>

<div class="container mx-auto px-4 py-8">
  <h1 class="text-4xl font-bold mb-4">My Projects</h1>
  <p class="text-lg mb-8">Here are some of my recent projects:</p>

  <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
    <div class="card bg-base-100 shadow-xl">
      <div class="card-body">
        <h2 class="card-title">Magees</h2>
        <p>A store with herbal stimulants, utilizing stripe, nextjs.</p>
        <div class="card-actions justify-end">
          <a href="projects/magees" class="btn btn-primary">View Project</a>
        </div>
      </div>
    </div>

    <div class="card bg-base-100 shadow-xl">
      <div class="card-body">
        <h2 class="card-title">Allstake</h2>
        <p>Web3 platform utilizing Thirdweb, Moralis, NextJs.</p>
        <div class="card-actions justify-end">
          <a href="projects/allstake" class="btn btn-primary">View Project</a>
        </div>
      </div>
    </div>

    <div class="card bg-base-100 shadow-xl">
      <div class="card-body">
        <h2 class="card-title">Cellular Domination Station</h2>
        <p>Game-of-life inspired game, built in 10 days for the Revival Game jam, using phaser and svelte.</p>
        <div class="card-actions justify-end">
          <a href="projects/cellular-domination-station" class="btn btn-primary">View Project</a>
        </div>
      </div>
    </div>

    <div class="card bg-base-100 shadow-xl">
      <div class="card-body">
        <h2 class="card-title">CrypTick</h2>
        <p>A crypto alert app built in rust, tauri and svelte.</p>
        <div class="card-actions justify-end">
          <a href="projects/cryptick" class="btn btn-primary">View Project</a>
        </div>
      </div>
    </div>
  </div>
</div>
