<script lang="ts">
  import "../app.css";

  import Tabs from "./Tabs.svelte";

  import { onMount } from "svelte";
  import { fade } from "svelte/transition";
  import { Avatar } from "@skeletonlabs/skeleton-svelte";

  let { children } = $props();

  let ready = $state(false);
  onMount(() => (ready = true));
</script>

<div class="page-container">
  {#if ready}
    <div class="w-full" in:fade={{ duration: 500, delay: 100 }}>
      <header class="sticky top-0 z-50 place-self-center lg:w-1/2">
        <div
          class="container mx-auto grid grid-cols-[1fr_auto] content-center gap-2 p-2"
        >
          <div class="grid grid-cols-[auto_auto_1fr] items-center gap-2">
            <a
              href="/"
              class="font-[Markazi_Text] text-3xl md:text-4xl font-extrabold md:visible text-surface-950-50"
            >
              <p>Rogue-like Algebra</p>
            </a>

            <span
              class="vr border-l-2 invisible w-0 md:visible md:w-auto rem border-surface-200-700"
            ></span>

            <p
              class="invisible w-0 md:visible md:w-auto text-xs text-surface-500"
            >
              by the Gold Team
            </p>
          </div>

          <div class="mx-auto grid grid-cols-2 items-center gap-2">
            <a href="https://odu.edu" class="drop-shadow-lg/30">
              <Avatar src="odu.jpg" name="ODU" />
            </a>
            <a href="https://cs.odu.edu" class="drop-shadow-lg/30">
              <Avatar src="odu_cs.jpg" name="CS ODU" />
            </a>
          </div>
        </div>
      </header>

      <div class="preset-gradient w-full rounded-container"><Tabs /></div>

      <div
        class="@container/main justify-self-center mt-5 w-4/5 md:w-3/5 lg:1/2"
      >
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
    background-color: var(--color-surface-50-950);
    min-height: calc(100vh - 1rem);
    min-width: calc(100vw - 1rem);
    margin: 0.5rem;
    padding: 0.5rem;
    border-radius: 0.5rem;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .preset-gradient {
    background-image: linear-gradient(
      45deg,
      var(--color-primary-500),
      var(--color-tertiary-500)
    );
    color: var(--color-primary-contrast-500);
  }
</style>
