<script lang="ts">
  import "../app.css";

  import Tabs from "./Tabs.svelte";

  import { Avatar } from "@skeletonlabs/skeleton-svelte";
</script>

<header class="sticky top-0 z-50 px-5 mb-2 backdrop-blur-md rounded-3xl">
  <div class="grid grid-cols-[1fr_auto] gap-2 py-5">
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

      <p class="invisible w-0 md:visible md:w-auto text-xs text-surface-500">
        by the <span
          class="font-semibold text-shadow-[0_0_20px_rgba(0,0,0,0)] text-shadow-amber-400/30"
          >Gold</span
        > Team
      </p>
    </div>

    <div class="grid grid-cols-2 gap-2">
      <a href="https://odu.edu" class="drop-shadow-lg/30">
        <Avatar src="/img/odu.jpg" name="ODU" />
      </a>
      <a href="https://cs.odu.edu" class="drop-shadow-lg/30">
        <Avatar src="/img/odu_cs.jpg" name="CS ODU" />
      </a>
    </div>
  </div>
  <Tabs />
</header>

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
