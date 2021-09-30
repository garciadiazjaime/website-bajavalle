<script>
  import { onMount } from 'svelte';

  export let images
  let Carousel;

  onMount(async () => {
    const module = await import('svelte-carousel');
    Carousel = module.default;
  });
</script>

<style>
img {
  width: 100%;
  height: auto;
}

.container {
  width: auto;
  height: 250px;
  overflow: hidden;
}
</style>

<div class="container">
  {#if Array.isArray(images) && images.length}
    <svelte:component this={Carousel} arrows={false}>
      {#each images as src}
        <img src={src} alt="title" />
      {/each}
    </svelte:component>
  {/if}
</div>
