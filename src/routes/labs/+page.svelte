<script lang="ts">
  import PageTitle from "../PageTitle.svelte";
  import Labs from "./Labs.svelte";
</script>

<svelte:head>
  <PageTitle page={"Labs"} />
</svelte:head>

<div>
  <div class="grid grid-cols-[auto_1fr] p-2 w-full">
    <header
      class="h2 px-5 [writing-mode:vertical-lr] rotate-180 place-self-start"
    >
      Lab Documents
    </header>
    <article class="text-justify pl-5 text-base xl:text-lg w-full flex-1">
      <div
        class="card preset-filled-surface-50-950 border-surface-200-800 divide-surface-200-800 block divide-y overflow-hidden"
      >
        <Labs />
      </div>
    </article>
  </div>
</div>
