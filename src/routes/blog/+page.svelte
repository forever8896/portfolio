<script lang="ts">
  interface BlogPost {
    slug: string;
    title: string;
    date: string;
    image: string;
    excerpt: string;
  }

  const posts: BlogPost[] = [
    {
      slug: "revival-game-jam-post-mortem",
      title: "Post Mortem: First Game Jam",
      image: "/images/blog/post-mortem/banner.webp",
      date: "2023-10-22",
      excerpt: "I took a challenge to make a game in 10 days for the Revival Game Jam 2024. Here's a post-mortem of the experience."
    },
  
    // Add more blog posts here
  ];

  posts.sort((a, b) => new Date(b.date).getTime() - new Date(a.date).getTime());
</script>

<svelte:head>
  <title>Blog</title>
</svelte:head>

<div class="container mx-auto px-4 sm:px-6 lg:px-8 py-8">
  <h1 class="text-3xl sm:text-4xl font-bold mb-6 sm:mb-8 text-center">Blog Posts</h1>
  <div class="grid gap-6 grid-cols-1 sm:grid-cols-2 lg:grid-cols-3">
    {#each posts as post}
      <a href="/blog/{post.slug}" class="card bg-base-100 shadow-xl hover:shadow-2xl transition-shadow border border-primary">
        <div class="card-body">
          <img src={post.image} alt={post.title} class="w-full h-48 object-cover mb-4 rounded-lg" />
          <h2 class="card-title text-xl sm:text-2xl">{post.title}</h2>
          <p class="text-sm text-primary">{new Date(post.date).toLocaleDateString()}</p>
          <p class="mt-2 text-sm sm:text-base">{post.excerpt}</p>
        </div>
      </a>
    {/each}
  </div>
</div>
