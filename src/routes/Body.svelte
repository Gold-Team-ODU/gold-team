<script lang="ts">
  let { children } = $props();
</script>

<main class="mx-auto px-5 w-full h-full">
  {@render children?.()}
</main>
