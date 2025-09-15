<script lang="ts">
  import { Tabs } from "@skeletonlabs/skeleton-svelte";

  let group = $state("lab_1_outline");
</script>

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
