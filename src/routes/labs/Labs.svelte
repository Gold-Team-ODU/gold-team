<script lang="ts">
  import { Tabs } from "@skeletonlabs/skeleton-svelte";

  let group = $state("lab_1_outline");
</script>

<div
  class="card preset-filled-surface-50-950 border-surface-200-800 divide-surface-200-800 block divide-y overflow-hidden"
>
  <Tabs value={group} onValueChange={(e) => (group = e.value)} fluid>
    {#snippet list()}
      <Tabs.Control value="lab_1_outline">Lab 1 Outline</Tabs.Control>
    {/snippet}
    {#snippet content()}
      <Tabs.Panel value="lab_1_outline">
        <article class="text-justify space-y-2 p-4">
          <iframe
            src="https://docs.google.com/document/d/e/2PACX-1vQOmUq5oIOYB-PJYY6zwtcVI1shSL-poTObS2IZOUonHDsVfZXYODo27FMYxChgeraYgyCY_BtbYsWa/pub?embedded=true"
            title="Lab 1 Outline"
            class="container h-[calc(100vh-25rem)]"
            allowfullscreen
          ></iframe>
        </article>
      </Tabs.Panel>
    {/snippet}
  </Tabs>
</div>
