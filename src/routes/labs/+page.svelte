<script lang="ts">
  import { Tabs } from "@skeletonlabs/skeleton-svelte";
  import PageTitle from "../PageTitle.svelte";
  import Placeholder from "../Placeholder.svelte";

  let group = $state("lab_1_outline");
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
        <Tabs value={group} onValueChange={(e) => (group = e.value)} fluid>
          {#snippet list()}
            <Tabs.Control value="lab_1_outline">
              <header class="h4">Lab 1 Outline</header>
            </Tabs.Control>
          {/snippet}
          {#snippet content()}
            <Tabs.Panel value="lab_1_outline">
              <article class="text-justify text-lg p-5">
                <iframe
                  src="https://docs.google.com/document/d/e/2PACX-1vQOmUq5oIOYB-PJYY6zwtcVI1shSL-poTObS2IZOUonHDsVfZXYODo27FMYxChgeraYgyCY_BtbYsWa/pub?embedded=true"
                  title="Lab 1 Outline"
                  class="w-full h-[calc(100vh-25rem)]"
                  allowfullscreen
                ></iframe>
              </article>
            </Tabs.Panel>
          {/snippet}
        </Tabs>
      </div>
    </article>
  </div>
</div>

<style>
</style>
