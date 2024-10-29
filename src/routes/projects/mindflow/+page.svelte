<script lang="ts">
    import { faCode, faLink, faUserShield } from '@fortawesome/free-solid-svg-icons';
    import { FontAwesomeIcon } from '@fortawesome/svelte-fontawesome';
    import { fade } from 'svelte/transition';
  </script>
  
  <div class="container mx-auto" in:fade={{ duration: 300 }}>
    <h1 class="text-4xl font-bold text-center mt-16 text-primary hover:underline hover:text-accent transition-all duration-300"> <a href="https://github.com/forever8896/mindflow" target="_blank">MindFlow</a></h1>
    <p class="text-center text-lg">October 25th 2024- Present</p>
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
            <li class="bg-base-100 p-4">Creating a simple private note taking and habit tracker.</li>
            <li class="bg-base-200 p-4">Using local storage to save the notes and habits.</li>
            <li class="bg-base-100 p-4">Styling and designing the app.</li>
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
            <li class="bg-base-100 p-4">Deepening my understanding of Rust.</li>
            <li class="bg-base-200 p-4">Publishing the code on github.</li>
            <li class="bg-base-100 p-4">Learning about local storage.</li>
            <li class="bg-base-200 p-4">Managing to build a working app.</li>
          </ul>
        </div>
      </div>
    </div>
  
    <div class="mt-12 space-y-8">
      <div class="card bg-base-300 shadow-xl mt-4">
        <div class="card-body">
          <h2 class="card-title text-2xl font-semibold text-secondary">About MindFlow</h2>
          <p class="text-lg leading-relaxed mt-2">Rust is slowly becoming my favorite language.</p>
          <p class="text-lg leading-relaxed mt-2">However, I still dont have enough practice to make it my go-to language.</p>
          <p class="text-lg leading-relaxed mt-2">Thats why I decided to make a simple note taking and habit tracker, to help me get more practice with Rust, and working with local storage.</p>
          <p class="text-lg leading-relaxed mt-2">The app contains a simple to-do list, note taking section, a pomodoro timer, and long term goal setting.</p>
          <p class="text-lg leading-relaxed mt-2">Every day, from the user behavior, the app pre-generates a journal entry, that the user can edit and write more information in.</p>
          <p class="text-lg leading-relaxed mt-2">The entire app data is stored in a single json file, the user can read it at any time, or delete it.</p>
        </div>
      </div>
      <div class="card bg-base-300 shadow-xl mt-4">
        <div class="card-body">
          <h2 class="card-title text-2xl font-semibold text-secondary">My Role</h2>
          <p class="text-lg leading-relaxed mt-2">Building the app from start to finish.</p>
          <p class="text-lg leading-relaxed mt-2">Testing the functionality and making sure its reliable.</p>
          <p class="text-lg leading-relaxed mt-2">Designing the app.</p>
        </div>
      </div>
      <div class="card bg-base-300 shadow-xl mt-4">
        <div class="card-body">
          <h2 class="card-title text-2xl font-semibold text-secondary">The technologies</h2>
          <p class="text-lg leading-relaxed mt-2">Tauri and Rust for the entire project</p>
          <p class="text-lg leading-relaxed mt-2">Svelte for the UI.</p>
        </div>
      </div>
      <div class="card bg-base-300 shadow-xl mt-4">
        <div class="card-body">
          <h2 class="card-title text-2xl font-semibold text-secondary">The Vision</h2>
          <p class="text-lg leading-relaxed mt-2">I want to make this my go-to note taking and habit tracker.</p>
          <p class="text-lg leading-relaxed mt-2">So as I use it, I will keep discovering new things to improve it in.</p>
        </div>
      </div>
      <h1 class="text-2xl font-semibold text-center mt-8 text-primary">The app is open source, and you can find the code here:</h1>
      <div class="flex justify-center">
      <p> <a href="https://github.com/forever8896/mindflow" class="text-white text-lg hover:text-accent hover:underline transition-all duration-300">MindFlow</a></p>
      </div>
    </div>
  </div>
  