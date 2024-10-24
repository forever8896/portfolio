<script lang="ts">
  import { faCode, faLink, faUserShield } from '@fortawesome/free-solid-svg-icons';
  import { FontAwesomeIcon } from '@fortawesome/svelte-fontawesome';
</script>

<div class="container mx-auto">
  <h1 class="text-4xl font-bold text-center mt-16 text-primary hover:underline hover:text-accent transition-all duration-300"> <a href="https://allstake.io" target="_blank">Allstake</a></h1>
  <p class="text-center text-lg">April 2024- Present</p>
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
          <li class="bg-base-100 p-4">Full stack development of entire platform</li>
          <li class="bg-base-200 p-4">Smart contract integration</li>
          <li class="bg-base-100 p-4">User authentication</li>
          <li class="bg-base-200 p-4">Staking functionality</li>
          <li class="bg-base-100 p-4">Real-time blockchain data fetching</li>
          <li class="bg-base-200 p-4">Deployment of new functionalities for each partner.</li>
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
          <li class="bg-base-200 p-4">Typescript</li>
          <li class="bg-base-100 p-4">Thirdweb</li>
          <li class="bg-base-200 p-4">Moralis</li>
          <li class="bg-base-100 p-4">Solidity (for smart contracts)</li>
          <li class="bg-base-200 p-4">TailwindCSS + DaisyUI</li>
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
          <li class="bg-base-100 p-4">+100 daily active users</li>
          <li class="bg-base-200 p-4">17 partners across 3 blockchains</li>
          <li class="bg-base-100 p-4">Sold out NFT collections.</li>
          <li class="bg-base-200 p-4">NFT Marketplaces</li>
          <li class="bg-base-100 p-4">NFT Auctions</li>
          <li class="bg-base-200 p-4">Raffles utilizing the Witnet oracle for randomness</li>
          <li class="bg-base-100 p-4">Non-custodial NFT Staking</li>
          <li class="bg-base-200 p-4">ERC-20 Token staking</li>
        </ul>
      </div>
    </div>
  </div>

  <div class="mt-12 space-y-8">
    <div class="card bg-base-300 shadow-xl mt-4">
      <div class="card-body">
        <h2 class="card-title text-2xl font-semibold text-secondary">About Allstake</h2>
        <p class="text-lg leading-relaxed mt-2">In April I started working on Allstake. The goal of the platform is to help every individual with a creative project vision.</p>
        <p class="text-lg leading-relaxed mt-2">Our partners are creators that want to leave a mark in the web3 space, but lack the technical knowledge to build utilities and experiences for their community.</p>
        <p class="text-lg leading-relaxed mt-2">Our users are the creators' community, who visit the platform to explore the utilities and experiences we have to offer.</p>
        <p class="text-lg leading-relaxed mt-2">The platform keeps growing every day, and the list of work and ideas to implement just keeps growing.</p>
      </div>
    </div>
    <div class="card bg-base-300 shadow-xl mt-4">
      <div class="card-body">
        <h2 class="card-title text-2xl font-semibold text-secondary">My Role</h2>
        <p class="text-lg leading-relaxed mt-2">I'm the full stack developer for the project, which means I'm responsible for the development of the entire platform.</p>
        <p class="text-lg leading-relaxed mt-2">Its a never-ending learning experience, as different partners have different needs and requirements, so the individual approach for each partner is expanding my knowledge and skills.</p>
        <p class="text-lg leading-relaxed mt-2">I'm also responsible for the maintenance of the platform, as well as the deployment of new functionalities for each partner, as well as customer support.</p>
      </div>
    </div>
    <div class="card bg-base-300 shadow-xl mt-4">
      <div class="card-body">
        <h2 class="card-title text-2xl font-semibold text-secondary">The technologies</h2>
        <p class="text-lg leading-relaxed mt-2">The platform is built with NextJS, Typescript, Thirdweb, Moralis, and TailwindCSS + DaisyUI.</p>
        <p class="text-lg leading-relaxed mt-2">We are utilizing Thirdweb for the smart contract development and deployment, Moralis for the blockchain integration, and NextJS for the frontend development.</p>
        <p class="text-lg leading-relaxed mt-2">The platform has been selected into the Thirdweb Startup Program, a 6 week learning experience to help us get familiar with the offerings from Thirdweb.</p>
        <p class="text-lg leading-relaxed mt-2">TailwindCSS and DaisyUI are used for the styling of the platform.</p>
      </div>
    </div>
    <div class="card bg-base-300 shadow-xl mt-4">
      <div class="card-body">
        <h2 class="card-title text-2xl font-semibold text-secondary">The Vision</h2>
        <p class="text-lg leading-relaxed mt-2">There are lots of platforms in existence offering utilities to web3 collectors, but from our experience, they often lack the individual approach for each creator.</p>
        <p class="text-lg leading-relaxed mt-2">We want to change that, and offer a platform that is flexible and customizable for each creator, while also offering a wide range of utilities and experiences.</p>
        <p class="text-lg leading-relaxed mt-2">We want to make the gap between an idea and a fully functional project as small as possible.</p>
      </div>
    </div>
  </div>
</div>
