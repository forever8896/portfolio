<script lang="ts">
  export let title: string;
  export let date: string;
</script>

<svelte:head>
  <title>{title}</title>
</svelte:head>

<article class="container mx-auto px-4 py-8 max-w-3xl">
  <h1 class="text-4xl font-bold mb-4">{title}</h1>
  <p class="text-sm text-primary mb-8">{new Date(date).toLocaleDateString()}</p>

  <div class="prose lg:prose-xl max-w-none">
    <slot />
  </div>
</article>

<style>
  :global(.prose h2) {
    @apply text-2xl font-semibold mt-8 mb-4 text-primary;
  }

  :global(.prose p) {
    @apply mb-4;
  }

  :global(.prose ul) {
    @apply list-disc list-inside mb-4;
  }

  :global(.prose li) {
    @apply mb-2;
  }

  :global(.prose img) {
    @apply mx-auto my-8 rounded-lg shadow-lg max-w-full h-auto;
  }

  :global(.prose figure) {
    @apply my-8;
  }

  :global(.prose figure img) {
    @apply mb-2;
  }

  :global(.prose figcaption) {
    @apply text-center text-sm text-secondary italic;
  }


  :global(.prose a) {
    @apply text-primary;
  }
</style>
