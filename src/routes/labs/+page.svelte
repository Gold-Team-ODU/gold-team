<script lang="ts">
  import PageTitle from "../PageTitle.svelte";
  import Labs from "./Labs.svelte";
</script>

<svelte:head>
  <PageTitle page={"Labs"} />
</svelte:head>

<div class="mx-auto">
  <div class="container grid grid-cols-[auto_1fr] p-2">
    <header
      class="h2 px-5 [writing-mode:vertical-lr] rotate-180 place-self-start"
    >
      Lab Documents
    </header>
    <article class="text-justify pl-5 text-base xl:text-lg">
      <Labs />
    </article>
  </div>
</div>
