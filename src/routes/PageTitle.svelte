<script lang="ts">
  let { page = "" } = $props();
</script>

{#if page === ""}
  <title>Rogue-like Algebra</title>
{:else}
  <title>Rogue-like Algebra | {page}</title>
{/if}
