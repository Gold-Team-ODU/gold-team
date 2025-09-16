<script lang="ts">
  import { Tabs } from "@skeletonlabs/skeleton-svelte";

  let group = $state("problem");
</script>

<div
  class="card preset-filled-surface-50-950 border-surface-200-800 divide-surface-200-800 block divide-y overflow-hidden"
>
  <Tabs value={group} onValueChange={(e) => (group = e.value)} fluid>
    {#snippet list()}
      <Tabs.Control value="problem">Problem</Tabs.Control>
      <Tabs.Control value="solution">Solution</Tabs.Control>
    {/snippet}
    {#snippet content()}
      <Tabs.Panel value="problem">
        <article class="text-justify space-y-2 p-4 pt-2">
          <p>
            <span class="font-bold">Algebra</span>, while being a very useful
            skill for daily life and forming the backbone of mathematics, is
            <span class="font-bold">extremely difficult</span> for the average person
            to understand.
          </p>
        </article>
      </Tabs.Panel>
      <Tabs.Panel value="solution">
        <article class="text-justify space-y-2 p-4 pt-2">
          <p>
            A <span class="font-bold">solo, turn-based, rogue-like game</span>
            where the player adventures through dungeons, tackling enemies and increasing
            in power and algebraic knowledge as they adventure along.
          </p>
        </article>
      </Tabs.Panel>
    {/snippet}
  </Tabs>
</div>
