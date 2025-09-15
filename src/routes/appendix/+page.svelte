<script lang="ts">
  import { Tabs } from "@skeletonlabs/skeleton-svelte";
  import PageTitle from "../PageTitle.svelte";
  import References from "./References.svelte";
  import Glossary from "./Glossary.svelte";

  let group = $state("references");
</script>

<svelte:head>
  <PageTitle page={"Appendix"} />
</svelte:head>

<div>
  <div class="grid grid-cols-[auto_1fr] p-2">
    <header
      class="h2 px-5 [writing-mode:vertical-lr] rotate-180 place-self-start"
    >
      Extra Resources
    </header>
    <article class="pl-5 text-base xl:text-lg">
      <div
        class="card preset-filled-surface-50-950 border-surface-200-800 divide-surface-200-800 block divide-y overflow-hidden"
      >
        <Tabs value={group} onValueChange={(e) => (group = e.value)} fluid>
          {#snippet list()}
            <Tabs.Control value="references">
              <header class="h4">References</header>
            </Tabs.Control>
            <Tabs.Control value="glossary">
              <header class="h4">Glossary</header>
            </Tabs.Control>
          {/snippet}
          {#snippet content()}
            <Tabs.Panel value="references">
              <article class="text-lg p-5">
                <References />
              </article>
            </Tabs.Panel>
            <Tabs.Panel value="glossary">
              <article class="text-lg p-5">
                <Glossary />
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
