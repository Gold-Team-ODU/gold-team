<script lang="ts">
  import { onMount } from "svelte";
  import { fade } from "svelte/transition";

  import favicon from "$lib/assets/favicon.png";

  let { children } = $props();

  let ready = $state(false);
  onMount(() => (ready = true));
</script>

<svelte:head>
  <link rel="icon" href={favicon} />
</svelte:head>

<div class="page-container">
  {#if ready}
    <div class="visible-on-mount" in:fade={{ duration: 250, delay: 250 }}>
      <div class="center-container">
        <span class="title">Rogue-like Algebra</span>
        {@render children?.()}
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

  .page-container {
    box-sizing: border-box;
    background-color: var(--mantle);
    min-height: calc(
      100vh - 1rem
    ); /* Make it at least the height of the viewport */
    width: 100%; /* Make it take up the full width */
    padding: 1rem;
    border-radius: 0.5rem;
    display: flex; /* Use flexbox to control content layout */
    flex-direction: column; /* Stack content vertically */
    align-items: center; /* Center content horizontally */
  }

  .center-container {
    box-sizing: border-box;
    background-color: var(--crust);
    width: 75vw; /* Make it take up the full width */
    padding: 1rem;
    border-radius: 0.5rem;
    display: flex; /* Use flexbox to control content layout */
    flex-direction: column; /* Stack content vertically */
    align-items: center; /* Center content horizontally */
  }

  .title {
    color: var(--text);
    font-family: "Markazi Text";
  }
</style>
