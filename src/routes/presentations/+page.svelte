<script lang="ts">
  import PageTitle from "../PageTitle.svelte";
  import Presentations from "./Presentations.svelte";
</script>

<svelte:head>
  <PageTitle page={"Presentations"} />
</svelte:head>

<div>
  <div class="grid grid-cols-[auto_1fr] p-2">
    <header
      class="h2 px-5 [writing-mode:vertical-lr] rotate-180 place-self-start"
    >
      Presentations
    </header>
    <article class="text-justify pl-5 text-base xl:text-lg">
      <div
        class="card preset-filled-surface-50-950 border-surface-200-800 divide-surface-200-800 block divide-y overflow-hidden"
      >
        <Presentations />
      </div>
    </article>
  </div>
</div>
