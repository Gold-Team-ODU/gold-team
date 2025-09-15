<script lang="ts">
  const items: number[] = [0, 1, 2, 3, 4];
</script>

<div class="space-y-4">
  <div class="placeholder animate-pulse"></div>
  <div class="grid grid-cols-4 gap-4">
    {#each [0, 1, 2, 3] as _}
      <div class="placeholder animate-pulse"></div>
    {/each}
  </div>
  <div class="placeholder animate-pulse"></div>
  <div class="placeholder animate-pulse"></div>
</div>
