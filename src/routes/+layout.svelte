<script lang="ts">
  import "../app.css";
  import { onMount } from "svelte";
  import { fade } from "svelte/transition";
  import { Avatar } from "@skeletonlabs/skeleton-svelte";

  let { children } = $props();

  let ready = $state(false);
  onMount(() => (ready = true));
</script>

<div class="page-container">
  {#if ready}
    <div class="visible-on-mount" in:fade={{ duration: 500, delay: 100 }}>
      <header class="sticky top-0 z-50 shadow-xl">
        <div
          class="container mx-auto grid grid-cols-[1fr_auto] items-center gap-10 p-2"
        >
          <h1 class="title">Rogue-like Algebra</h1>
          <div class="container mx-auto grid grid-cols-2 items-center gap-2">
            <a href="https://odu.edu" target="_blank">
              <Avatar src="odu.jpg" name="ODU" />
            </a>
            <a href="https://cs.odu.edu" target="_blank">
              <Avatar src="odu_cs.jpg" name="CS ODU" />
            </a>
          </div>
        </div>
      </header>

      <div class="center-container">
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
    font-size: 2.5rem;
  }
</style>
