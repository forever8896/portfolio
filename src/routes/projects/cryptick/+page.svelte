<script lang="ts">
    import { faCode, faLink, faUserShield } from '@fortawesome/free-solid-svg-icons';
    import { FontAwesomeIcon } from '@fortawesome/svelte-fontawesome';
    import { fade } from 'svelte/transition';
  </script>
  
  <div class="container mx-auto" in:fade={{ duration: 300 }}>
    <h1 class="text-4xl font-bold text-center mt-16 text-primary hover:underline hover:text-accent transition-all duration-300"> <a href="https://github.com/forever8896/crypto_alerts_tauri" target="_blank">CrypTick</a></h1>
    <p class="text-center text-lg">October 3th 2024- Present</p>
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
            <li class="bg-base-100 p-4">Creating a crypto alerts app using Rust.</li>
            <li class="bg-base-200 p-4">Using real-time updates from the Binance public websocket API.</li>
            <li class="bg-base-100 p-4">Styling and designing the app.</li>
            <li class="bg-base-200 p-4">Creating and selecting the sounds for the app.</li>
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
            <li class="bg-base-100 p-4">Rust</li>
            <li class="bg-base-200 p-4">Tauri</li>
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
            <li class="bg-base-100 p-4">Learning Rust and Tauri a bit.</li>
            <li class="bg-base-200 p-4">Publishing the code on github.</li>
            <li class="bg-base-100 p-4">Learning about websocket APIs.</li>
            <li class="bg-base-200 p-4">Managing to build a working app.</li>
          </ul>
        </div>
      </div>
    </div>
  
    <div class="mt-12 space-y-8">
      <div class="card bg-base-300 shadow-xl mt-4">
        <div class="card-body">
          <h2 class="card-title text-2xl font-semibold text-secondary">About CrypTick</h2>
          <p class="text-lg leading-relaxed mt-2">A friend introduced me to rust, and ever since opening the rust book, I have felt a passion for the language.</p>
          <p class="text-lg leading-relaxed mt-2">However, at the 7th chapter of the book I grew impatient and hungry for experience .</p>
          <p class="text-lg leading-relaxed mt-2">Thats when I discovered Tauri, and its clear documentation allowed me to jump in and start building.</p>
        </div>
      </div>
      <div class="card bg-base-300 shadow-xl mt-4">
        <div class="card-body">
          <h2 class="card-title text-2xl font-semibold text-secondary">My Role</h2>
          <p class="text-lg leading-relaxed mt-2">Building the app from start to finish.</p>
          <p class="text-lg leading-relaxed mt-2">Testing the functionality and making sure its reliable.</p>
          <p class="text-lg leading-relaxed mt-2">Design and picking of fun sounds..</p>
        </div>
      </div>
      <div class="card bg-base-300 shadow-xl mt-4">
        <div class="card-body">
          <h2 class="card-title text-2xl font-semibold text-secondary">The technologies</h2>
          <p class="text-lg leading-relaxed mt-2">Tauri and Rust for the entire project</p>
          <p class="text-lg leading-relaxed mt-2">Svelte for the UI.</p>
          <p class="text-lg leading-relaxed mt-2">Binance websocket API for the real-time data.</p>
        </div>
      </div>
      <div class="card bg-base-300 shadow-xl mt-4">
        <div class="card-body">
          <h2 class="card-title text-2xl font-semibold text-secondary">The Vision</h2>
          <p class="text-lg leading-relaxed mt-2">I want to continue learning Rust and Tauri, the obvious next step is to learn how to make it a phone app as well.</p>
          <p class="text-lg leading-relaxed mt-2">With the stable price alert logic, I can easily connect it to a different websocket API, and make it a stock alerts app.</p>
        </div>
      </div>
      <h1 class="text-2xl font-semibold text-center mt-8 text-primary">The app is open source, and you can find the code here:</h1>
      <div class="flex justify-center">
      <p> <a href="https://github.com/forever8896/crypto_alerts_tauri" class="text-white text-lg hover:text-accent hover:underline transition-all duration-300">CrypTick</a></p>
      </div>
    </div>
  </div>
  