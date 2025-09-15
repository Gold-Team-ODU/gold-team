<script>
  import {
    Album,
    FlaskConical,
    House,
    Presentation,
    Users,
  } from "@lucide/svelte";
</script>

<aside class="w-[calc(100%_-_1rem)] relative place-self-center">
  <!-- Gradient shadow thanks to https://ibelick.com/blog/create-gradient-shadows-tailwind-css -->
  <div
    class="absolute -inset-1.5 rounded-3xl preset-gradient opacity-75 blur"
  ></div>
  <div class="rounded-3xl relative preset-tonal-primary">
    <div class="place-self-center">
      <div
        class="grid grid-cols-5 gap-10 md:gap-5 p-2 place-items-center bg-gradient-to-r from-primary-contrast-200-800 to-tertiary-contrast-200-800 text-transparent bg-clip-text"
      >
        <a
          href="/"
          class="grid grid-cols-[auto_1fr] gap-0.5 hover:text-surface-contrast-50-950"
          title="Home"
        >
          <span class="material-symbols-rounded"> home </span>
          <div class="max-md:invisible max-md:w-0">Home</div>
        </a>
        <a
          href="/presentations"
          class="grid grid-cols-[auto_1fr] gap-0.5 hover:text-surface-contrast-50-950"
          title="Presentations"
        >
          <span class="material-symbols-rounded"> monitor </span>
          <div class="max-md:invisible max-md:w-0">Presentations</div>
        </a>
        <a
          href="/labs"
          class="grid grid-cols-[auto_1fr] gap-0.5 hover:text-surface-contrast-50-950"
          title="Labs"
        >
          <span class="material-symbols-rounded"> experiment </span>
          <div class="max-md:invisible max-md:w-0">Labs</div>
        </a>
        <a
          href="/appendix"
          class="grid grid-cols-[auto_1fr] gap-0.5 hover:text-surface-contrast-50-950"
          title="Appendix"
        >
          <span class="material-symbols-rounded"> book </span>
          <div class="max-md:invisible max-md:w-0">Appendix</div>
        </a>
        <a
          href="/team"
          class="grid grid-cols-[auto_1fr] gap-0.5 hover:text-surface-contrast-50-950"
          title="Team"
        >
          <span class="material-symbols-rounded"> group </span>
          <div class="max-md:invisible max-md:w-0">Team</div>
        </a>
      </div>
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
