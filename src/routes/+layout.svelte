<script lang="ts">
  import "../app.css";

  import { onMount } from "svelte";
  import { fade } from "svelte/transition";

  import TitleBar from "./TitleBar.svelte";
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
      class="container mx-auto z-[-1] min-h-screen place-self-center max-w-xl md:max-w-4xl 2xl:max-w-7xl bg-surface-100-900 drop-shadow-[0_0_30px_rgba(0,0,0,0)] drop-shadow-surface-500/80 rounded-3xl"
      in:fade={{ duration: 500, delay: 100 }}
    >
      <div class="z-1 min-h-screen grid grid-rows-[auto_1fr_auto] gap-5">
        <TitleBar />

        <main class="mx-auto px-5 w-full h-full">
          {@render children?.()}
        </main>

        <Footer />
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
