<script lang="ts">
  import "../app.css";
  import { onMount } from "svelte";
  import { fade } from "svelte/transition";

  let { children } = $props();

  let ready = $state(false);
  onMount(() => (ready = true));
</script>

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
    background-color: var(--color-ctp-mantle);
    min-height: calc(100vh - 1rem);
    min-width: calc(100vw - 1rem);
    margin: 0.5rem;
    padding: 0.5rem;
    border-radius: 0.5rem;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .center-container {
    box-sizing: border-box;
    background-color: var(--color-ctp-crust);
    width: 75vw;
    padding: 1rem;
    border-radius: 0.5rem;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .title {
    color: var(--color-ctp-text);
    font-family: "Markazi Text";
  }
</style>
