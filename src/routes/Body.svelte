<script lang="ts">
  let { children } = $props();
</script>

<main class="mx-auto p-5 w-full">
  {@render children?.()}
</main>
