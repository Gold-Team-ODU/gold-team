<script>
  import { House, Users } from "@lucide/svelte";
</script>

<aside class="preset-gradient justify-self-center rounded-container w-full">
  <div class="place-self-center">
    <div class="grid grid-cols-3 gap-20 p-2">
      <a
        href="/"
        class="anchor grid grid-cols-[auto_1fr] gap-0.5 text-surface-50"
      >
        <House />
        Home
      </a>
      <a
        href="/"
        class="anchor grid grid-cols-[auto_1fr] gap-0.5 text-surface-50"
      >
        <House />
        Home
      </a>
      <a
        href="/"
        class="anchor grid grid-cols-[auto_1fr] gap-0.5 text-surface-50"
      >
        <Users />
        Team
      </a>
    </div>
  </div>
</aside>

<style>
  .preset-gradient {
    background-image: linear-gradient(
      45deg,
      var(--color-primary-500),
      var(--color-tertiary-500)
    );
    color: var(--color-primary-contrast-500);
    backdrop-filter: blur(16px);
  }
</style>
