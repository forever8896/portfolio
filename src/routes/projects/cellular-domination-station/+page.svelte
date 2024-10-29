<script lang="ts">
    import { faCode, faLink, faUserShield } from '@fortawesome/free-solid-svg-icons';
    import { FontAwesomeIcon } from '@fortawesome/svelte-fontawesome';
    import { fade } from 'svelte/transition';
  </script>
  
  <div class="container mx-auto" in:fade={{ duration: 300 }}>
    <h1 class="text-4xl font-bold text-center mt-16 text-primary hover:underline hover:text-accent transition-all duration-300"> <a href="https://brianpistar.itch.io/cellular-domination-station" target="_blank">Cellular Domination Station</a></h1>
    <p class="text-center text-lg">October 12th 2024- October 21st 2024</p>
    <div class="divider"></div>
    
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 mt-8">
      <!-- Responsibilities Card -->
      <div class="card bg-base-200 shadow-xl">
        <figure class="px-10 pt-10">
          <FontAwesomeIcon icon={faCode} class="h-24 w-24 text-primary" />
        </figure>
        <div class="card-body">
          <h2 class="card-title text-secondary">Responsibilities</h2>
          <ul class="list-disc list-inside space-y-4">
            <li class="bg-base-100 p-4">Creating a simple game for a game jam within 10 days.</li>
            <li class="bg-base-200 p-4">Utilizing Phaser for the game development.</li>
            <li class="bg-base-100 p-4">Utilizing Svelte for the frontend development.</li>
            <li class="bg-base-200 p-4">Getting the game published on itch.io.</li>
          </ul>
        </div>
      </div>
  
      <!-- Technologies Card -->
      <div class="card bg-base-200 shadow-xl">
        <figure class="px-10 pt-10">
          <FontAwesomeIcon icon={faLink} class="h-24 w-24 text-secondary" />
        </figure>
        <div class="card-body">
          <h2 class="card-title text-secondary">Technologies</h2>
          <ul class="list-disc list-inside space-y-4">
            <li class="bg-base-100 p-4">Phaser</li>
            <li class="bg-base-200 p-4">Typescript</li>
            <li class="bg-base-100 p-4">Svelte</li>
          </ul>
        </div>
      </div>
  
      <!-- Results Card -->
      <div class="card bg-base-200 shadow-xl">
        <figure class="px-10 pt-10 ">
          <FontAwesomeIcon icon={faUserShield} class="h-24 w-24 text-accent" />
        </figure>
        <div class="card-body">
          <h2 class="card-title text-secondary">Results</h2>
          <ul class="list-disc list-inside space-y-4">
            <li class="bg-base-100 p-4">Getting the game published on itch.io.</li>
            <li class="bg-base-200 p-4">Receiving positive feedback from players.</li>
            <li class="bg-base-100 p-4">Learning about Phaser and Svelte..</li>
            <li class="bg-base-200 p-4">Managing to build a game in 10 days</li>
          </ul>
        </div>
      </div>
    </div>
  
    <div class="mt-12 space-y-8">
      <div class="card bg-base-300 shadow-xl mt-4">
        <div class="card-body">
          <h2 class="card-title text-2xl font-semibold text-secondary">About Cellular Domination Station</h2>
          <p class="text-lg leading-relaxed mt-2">Cellular Domination Station is a game inspired by Conway's Game of Life, built in Phaser and Svelte.</p>
          <p class="text-lg leading-relaxed mt-2">The goal of the game is to survive for as long as possible, while red enemy snakes keep approaching your base.</p>
          <p class="text-lg leading-relaxed mt-2">The game renders a grid of cells, and utilizes the rules of the game of life to create some fun chaos.</p>
        </div>
      </div>
      <div class="card bg-base-300 shadow-xl mt-4">
        <div class="card-body">
          <h2 class="card-title text-2xl font-semibold text-secondary">My Role</h2>
          <p class="text-lg leading-relaxed mt-2">Building the game from start to finish.</p>
          <p class="text-lg leading-relaxed mt-2">Picking royalty-free sounds and music.</p>
          <p class="text-lg leading-relaxed mt-2">Improving based on feedback..</p>
        </div>
      </div>
      <div class="card bg-base-300 shadow-xl mt-4">
        <div class="card-body">
          <h2 class="card-title text-2xl font-semibold text-secondary">The technologies</h2>
          <p class="text-lg leading-relaxed mt-2">Phaser and svelte with Typescript for the entire project</p>
          <p class="text-lg leading-relaxed mt-2">Vanilla CSS for the styling.</p>
          <p class="text-lg leading-relaxed mt-2">Music from <a href="https:/zapsplat.com" target="_blank" class="text-primary hover:text-accent hover:underline transition-all duration-300">ZapSplat</a></p>
          <p class="text-lg leading-relaxed mt-2">Sounds from <a href="https:/jsfxr.me" target="_blank" class="text-primary hover:text-accent hover:underline transition-all duration-300">JSFXR</a></p>
        </div>
      </div>
      <div class="card bg-base-300 shadow-xl mt-4">
        <div class="card-body">
          <h2 class="card-title text-2xl font-semibold text-secondary">The Vision</h2>
          <p class="text-lg leading-relaxed mt-2">I mostly wanted to challenge myself and see if I could build a game in 10 days.</p>
          <p class="text-lg leading-relaxed mt-2">I also wanted to learn more about Phaser and Svelte.</p>
        </div>
      </div>
      <h1 class="text-2xl font-semibold text-center mt-8 text-primary">You can play the game here:</h1>
      <div class="flex justify-center">
        <iframe frameborder="0" src="https://itch.io/embed/3053044?bg_color=000000&amp;fg_color=ffffff&amp;link_color=5bfa65&amp;border_color=000000" width="552" height="167"><a href="https://brianpistar.itch.io/cellular-domination-station">Cellular Domination Station by BrianPistar</a></iframe>
      </div>
    </div>
  </div>
  