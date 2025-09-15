<script lang="ts">
  import "../app.css";

  import { onMount } from "svelte";
  import { fade } from "svelte/transition";

  import Header from "./Header.svelte";
  import Footer from "./Footer.svelte";

  let ready = $state(false);
  onMount(() => {
    ready = true;
  });

  let { children } = $props();
</script>

<div class="w-full h-screen">
  {#if ready}
    <!-- Fade in content pane -->
    <div
      class="container mx-auto max-w-xl md:max-w-4xl 2xl:max-w-7xl"
      in:fade={{ duration: 500, delay: 100 }}
    >
      <div
        class="place-self-center w-full min-h-screen bg-surface-100-900 drop-shadow-[0_0_30px_rgba(0,0,0,0)] drop-shadow-surface-500/80 rounded-3xl"
      >
        <div class="min-h-screen grid grid-rows-[auto_1fr_auto] gap-5">
          <Header />

          <main class="mx-auto px-5 w-full h-full">
            {@render children?.()}
          </main>

          <Footer />
        </div>
      </div>
    </div>
  {/if}
</div>

<style>
  :global(#smui-app),
  :global(body),
  :global(html) {
    display: block !important;
    height: auto !important;
    width: auto !important;
    position: static !important;
  }
</style>
