<script lang="ts">
  import { Tabs } from "@skeletonlabs/skeleton-svelte";
  import PageTitle from "../PageTitle.svelte";

  let group = $state("societal_problem");
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
        <Tabs value={group} onValueChange={(e) => (group = e.value)} fluid>
          {#snippet list()}
            <Tabs.Control value="societal_problem">
              <header class="h4">Societal Problem</header>
            </Tabs.Control>
            <Tabs.Control value="feasibility">
              <header class="h4">Feasibility</header>
            </Tabs.Control>
            <Tabs.Control value="design">
              <header class="h4">Design</header>
            </Tabs.Control>
          {/snippet}
          {#snippet content()}
            <Tabs.Panel value="societal_problem">
              <article class="text-justify text-lg p-5">
                <embed
                  src="/presentations/societal_problem.pdf"
                  type="application/pdf"
                  class="w-full h-[calc(100vh-25rem)]"
                />
              </article>
            </Tabs.Panel>
            <Tabs.Panel value="feasibility">
              <article class="text-justify text-lg p-5">
                <embed
                  src="/presentations/feasibility.pdf"
                  type="application/pdf"
                  class="w-full h-[calc(100vh-25rem)]"
                />
              </article>
            </Tabs.Panel>
            <Tabs.Panel value="design">
              <article class="text-justify text-lg p-5">
                <embed
                  src="/presentations/formal_design.pdf"
                  type="application/pdf"
                  class="w-full h-[calc(100vh-25rem)]"
                />
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
