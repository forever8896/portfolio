<script lang="ts">
    import { fade } from 'svelte/transition';

  let skills = [
    {
      name: 'JavaScript',
      icon: "/images/icons/js.svg",
      proficiency: 90,
      experience: 85,
      enjoyment: 60,
      description: "My primary language for web development. I have extensive experience with modern ES6+ features, asynchronous programming, and frameworks like React and NextJS.",
      notes: "First language I ever learned, and quite an ever expanding rabbit hole it is."
    },
    {
      name: 'TypeScript',
      icon: "/images/icons/ts.svg",
      proficiency: 60,
      experience: 50,
      enjoyment: 70,
      description: "I use TypeScript in most of my projects for its strong typing and improved developer experience. It has greatly enhanced my ability to write maintainable code.",
      notes: "At first I hated TypeScript, but now I enjoy the readability of the code. It's become an essential tool in my development process, especially for larger projects.",
      visible: false
    },
    {
      name: 'React',
      icon: "/images/icons/react.svg",
      proficiency: 88,
      experience: 90,
      enjoyment: 50,
      description: "My go-to framework for building user interfaces. I'm proficient with hooks, managing state, and interacting with APIs.",
      notes: "Now the highest enjoyment for me, but I feel like React sometimes has to be learned in order to use many other libraries.",
      visible: false
    },
    {
      name: 'Svelte',
      icon: "/images/icons/svelte.svg",
      proficiency: 80,
      experience: 70,
      enjoyment: 95,
      description: "I've recently fallen in love with Svelte for its simplicity and performance. I've used it in several personal projects (including this website) and am excited about its future.",
      notes: "Svelte's approach to reactivity and its build-time compilation make it incredibly fast and enjoyable to work with. I'm particularly impressed with how it handles state management.",
      visible: false
    },
    {
      name: 'Go',
      icon: "/images/icons/golang.svg",
      proficiency: 40,
      experience: 30,
      enjoyment: 40,
      description: "I've been playing with Go for a while. Some small experimentations, but it has helped me understand how html gets to the browser, and the simplicity drew me towards it.",
      notes: "Go's simplicity and performance are what initially attracted me. While I'm still learning, I appreciate its strong standard library and concurrency model.",
      visible: false
    },
    {
      name: 'Rust',
      icon: "/images/icons/rust.svg",
      proficiency: 60,
      experience: 50,
      enjoyment: 95,
      description: "My latest programming passion. Without finishing the rust book, I jumped into creating my own GUI in tauri, which you can read more about <a href='/projects/cryptick' class='text-primary hover:underline'>here</a>.",
      notes: "Rust's focus on safety and performance is fascinating. While the learning curve is steep, I find the concepts of ownership and borrowing to be revolutionary in systems programming.",
      visible: false
    },
  ];
</script>

<style>
  @keyframes glow {
    0% {
      box-shadow: 0 0 5px #4f46e5, 0 0 10px #4f46e5, 0 0 15px #4f46e5, 0 0 20px #4f46e5;
    }
    50% {
      box-shadow: 0 0 10px #4f46e5, 0 0 20px #4f46e5, 0 0 30px #4f46e5, 0 0 40px #4f46e5;
    }
    100% {
      box-shadow: 0 0 5px #4f46e5, 0 0 10px #4f46e5, 0 0 15px #4f46e5, 0 0 20px #4f46e5;
    }
  }

  .ai-card {
    animation: glow 3s ease-in-out infinite;
  }
</style>

<div class="container mx-auto px-4 py-8" in:fade={{ duration: 300 }}>
  <h1 class="text-4xl font-bold mb-8 text-center">About Me</h1>
  
  <div class="card lg:card-side bg-base-100 shadow-xl mb-12">
    <figure class="lg:w-1/3">
      <img src="/images/profile.jpg" alt="Profile" class="rounded-lg m-6 w-64 h-64 object-cover" />
    </figure>
    <div class="card-body lg:w-2/3">
      <h2 class="card-title text-2xl">Brian Pistar</h2>
      <p class="text-lg mb-4">
        I am a software developer from the Czech Republic, and I am addicted to information. 
        With a passion for creating efficient and innovative solutions, I specialize in web development 
        and enjoy exploring new technologies. My journey in software development has led me to work 
        with a variety of languages and frameworks, each adding to my skillset and perspective on 
        problem-solving in the digital realm.
      </p>
      <p class="text-lg mb-4">
        Still, I don't consider myself a professional; I learn as I go.
      </p>
      <p class="text-lg mb-4">
        Without AI I would have had to go through a conventional learning experience, but AI allows me to learn by doing.
      </p>
    </div>
  </div>

  <h2 class="text-3xl font-semibold mb-6">My Skills</h2>
  <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
    {#each skills as skill}
      <div class="card bg-base-200 shadow-xl">
        <div class="card-body">
          <div class="flex items-center mb-4">
            <img src={skill.icon} alt={skill.name} class="w-16 h-16 mr-4" />
            <h3 class="card-title text-2xl">{skill.name}</h3>
          </div>
          <div class="mb-4">
            <label for="proficiency-{skill.name}" class="label">
              <span class="label-text">Proficiency</span>
              <span class="label-text-alt">{skill.proficiency}%</span>
            </label>
            <progress id="proficiency-{skill.name}" class="progress progress-primary w-full" value={skill.proficiency} max="100"></progress>
          </div>
          <div class="mb-4">
            <label for="experience-{skill.name}" class="label">
              <span class="label-text">Experience</span>
              <span class="label-text-alt">{skill.experience}%</span>
            </label>
            <progress id="experience-{skill.name}" class="progress progress-secondary w-full" value={skill.experience} max="100"></progress>
          </div>
          <div class="mb-4">
            <label for="enjoyment-{skill.name}" class="label">
              <span class="label-text">Enjoyment</span>
              <span class="label-text-alt">{skill.enjoyment}%</span>
            </label>
            <progress id="enjoyment-{skill.name}" class="progress progress-accent w-full" value={skill.enjoyment} max="100"></progress>
          </div>
          <p class="text-base mb-4">{@html skill.description}</p>
          <div class="divider">Notes</div>
          <p class="text-sm italic">{skill.notes}</p>
        </div>
      </div>
    {/each}
  </div>

  <!-- AI card -->
  <div class="mt-12">
    <div class="card bg-base-200 shadow-xl ai-card">
      <div class="card-body">
        <div class="flex items-center mb-4">
          <img src="/images/icons/ai.svg" alt="AI" class="w-24 h-24 mr-4" />
          <h3 class="card-title text-2xl">AI</h3>
        </div>
        <div class="mb-4">
          <label for="ai-proficiency" class="label">
            <span class="label-text">Proficiency</span>
            <span class="label-text-alt">100%</span>
          </label>
          <progress id="ai-proficiency" class="progress progress-primary w-full" value="100" max="100"></progress>
        </div>
        <div class="mb-4">
          <label for="ai-experience" class="label">
            <span class="label-text">Experience</span>
            <span class="label-text-alt">100%</span>
          </label>
          <progress id="ai-experience" class="progress progress-secondary w-full" value="100" max="100"></progress>
        </div>
        <div class="mb-4">
          <label for="ai-enjoyment" class="label">
            <span class="label-text">Enjoyment</span>
            <span class="label-text-alt">99.999%</span>
          </label>
          <progress id="ai-enjoyment" class="progress progress-accent w-full" value="99.999" max="100"></progress>
        </div>
        <p class="text-base mb-4">
          AI has revolutionized my approach to software development. It allows me to jump into any project, and learn along the way. I have been using AI since the public release of ChatGPT, pretty much every day. I enjoy claude sonnet 3.5, and cursor.
        </p>
        <div class="divider">Notes</div>
        <p class="text-sm italic">
          The rapid advancements in AI technology continually amaze me. I'm particularly excited about the potential of large language models and their applications in code generation and problem-solving. AI has become an indispensable tool in my development workflow, allowing me to learn and create more efficiently than ever before.
        </p>
      </div>
    </div>
  </div>
</div>
