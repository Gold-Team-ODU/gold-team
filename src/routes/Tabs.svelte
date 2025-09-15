<script>
  import {
    Album,
    FlaskConical,
    House,
    Presentation,
    Users,
  } from "@lucide/svelte";
</script>

<aside class="preset-gradient justify-self-center rounded-3xl w-full">
  <div class="place-self-center">
    <div class="grid grid-cols-5 gap-10 md:gap-5 p-2 place-items-center">
      <a
        href="/"
        class="anchor grid grid-cols-[auto_1fr] gap-0.5 text-surface-50"
        title="Home"
      >
        <House />
        <div class="max-md:invisible max-md:w-0">Home</div>
      </a>
      <a
        href="/presentations"
        class="anchor grid grid-cols-[auto_1fr] gap-0.5 text-surface-50"
        title="Presentations"
      >
        <Presentation />
        <div class="max-md:invisible max-md:w-0">Presentations</div>
      </a>
      <a
        href="/labs"
        class="anchor grid grid-cols-[auto_1fr] gap-0.5 text-surface-50"
        title="Labs"
      >
        <FlaskConical />
        <div class="max-md:invisible max-md:w-0">Labs</div>
      </a>
      <a
        href="/appendix"
        class="anchor grid grid-cols-[auto_1fr] gap-0.5 text-surface-50"
        title="Appendix"
      >
        <Album />
        <div class="max-md:invisible max-md:w-0">Appendix</div>
      </a>
      <a
        href="/team"
        class="anchor grid grid-cols-[auto_1fr] gap-0.5 text-surface-50"
        title="Team"
      >
        <Users />
        <div class="max-md:invisible max-md:w-0">Team</div>
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
