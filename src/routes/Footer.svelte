<script lang="ts">
  import LightSwitch from "./LightSwitch.svelte";
</script>

<footer class="mx-auto px-5 py-4 max-w-xl md:max-w-4xl 2xl:max-w-7xl">
  <span class="grid grid-cols-[auto_auto] items-center gap-2">
    <div class=" justify-self-start">
      <p class="mx-auto bg-surface-100-900 rounded-t">
        © 2025 Rogue-like Algebra
      </p>
    </div>

    <div class="justify-self-end">
      <LightSwitch />
    </div>
  </span>
</footer>
