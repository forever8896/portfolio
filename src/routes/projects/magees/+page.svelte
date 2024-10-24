<script lang="ts">
    import { faCode, faLink, faUserShield } from '@fortawesome/free-solid-svg-icons';
    import { FontAwesomeIcon } from '@fortawesome/svelte-fontawesome';
  </script>
  
  <div class="container mx-auto">
    <h1 class="text-4xl font-bold text-center mt-16 text-primary hover:underline hover:text-accent transition-all duration-300"> <a href="https://magees.cz" target="_blank">Magees</a></h1>
    <p class="text-center text-lg">2023-2024</p>
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
            <li class="bg-base-100 p-4">Creating a store with herbal stimulants.</li>
            <li class="bg-base-200 p-4">Design of site the store, the products, and the product etiquettes.</li>
            <li class="bg-base-100 p-4">Creating a connection with the stripe payment gateway.</li>
            <li class="bg-base-200 p-4">Utilizing the packeta API for shipping.</li>
            <li class="bg-base-100 p-4">Creating an SEO-optimized site and blog.</li>
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
            <li class="bg-base-100 p-4">NextJS</li>
            <li class="bg-base-200 p-4">TailwindCSS</li>
            <li class="bg-base-100 p-4">Framer Motion</li>
            <li class="bg-base-200 p-4">Stripe</li>
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
            <li class="bg-base-100 p-4">A fully functional store with a nice design.</li>
            <li class="bg-base-200 p-4">A connection with the stripe payment gateway.</li>
            <li class="bg-base-100 p-4">A connection with the packeta shipping API.</li>
            <li class="bg-base-200 p-4">A Mailing list connection with Ecomail.</li>
          </ul>
        </div>
      </div>
    </div>
  
    <div class="mt-12 space-y-8">
      <div class="card bg-base-300 shadow-xl mt-4">
        <div class="card-body">
          <h2 class="card-title text-2xl font-semibold text-secondary">About Magees</h2>
          <p class="text-lg leading-relaxed mt-2">As a Developer, I always want an extra pick-me-up.</p>
          <p class="text-lg leading-relaxed mt-2">I attempted to make a store with herbal stimulants.</p>
          <p class="text-lg leading-relaxed mt-2">I was responsible for the design of the site, the products, and the product etiquettes, as well as trying to run marketing for the store.</p>
        </div>
      </div>
      <div class="card bg-base-300 shadow-xl mt-4">
        <div class="card-body">
          <h2 class="card-title text-2xl font-semibold text-secondary">My Role</h2>
          <p class="text-lg leading-relaxed mt-2">Building the store from start to finish.</p>
          <p class="text-lg leading-relaxed mt-2">Design of the site, the products, and the product etiquettes.</p>
          <p class="text-lg leading-relaxed mt-2">Marketing of the store.</p>
        </div>
      </div>
      <div class="card bg-base-300 shadow-xl mt-4">
        <div class="card-body">
          <h2 class="card-title text-2xl font-semibold text-secondary">The technologies</h2>
          <p class="text-lg leading-relaxed mt-2">NextJS</p>
          <p class="text-lg leading-relaxed mt-2">TailwindCSS for the styling</p>
          <p class="text-lg leading-relaxed mt-2">Framer Motion for the animations</p>
          <p class="text-lg leading-relaxed mt-2">Stripe for the payment gateway</p>
        </div>
      </div>
      <div class="card bg-base-300 shadow-xl mt-4">
        <div class="card-body">
          <h2 class="card-title text-2xl font-semibold text-secondary">The Vision</h2>
          <p class="text-lg leading-relaxed mt-2">The store is still an unclosed chapter for me, I wasnt able to reach consistency with marketing and developer work.</p>
          <p class="text-lg leading-relaxed mt-2">I potentially want to continue working on the store in the future, but I am not sure if I will have the time yet.</p>
        </div>
      </div>
    
    </div>
  </div>
  