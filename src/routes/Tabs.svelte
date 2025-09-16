<aside class="mx-auto w-[calc(100%_-_1rem)]">
  <div class="relative">
    <!-- Gradient shadow thanks to https://ibelick.com/blog/create-gradient-shadows-tailwind-css -->
    <div
      class="absolute -inset-1.5 preset-gradient opacity-75 blur rounded-full"
    ></div>
    <!-- White shine -->
    <div
      class="absolute -inset-0 bg-surface-50 opacity-75 blur-[3px] rounded-full"
    ></div>
    <!-- Main tab bar -->
    <div class="relative preset-tonal-surface rounded-full">
      <!-- Center icons & cut out text (https://stackoverflow.com/a/71206137/17004103) -->
      <div
        class="place-self-center bg-gradient-to-r from-primary-contrast-200-800 to-tertiary-contrast-200-800 text-transparent bg-clip-text"
      >
        <div
          class="container grid grid-cols-[1fr_auto_auto_auto_auto_auto_1fr] gap-10 md:gap-5 p-2 place-items-center"
        >
          <br />
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
          <br />
        </div>
      </div>
    </div>
  </div>
</aside>

<style>
  .preset-gradient {
    background-image: linear-gradient(
      var(--rotate),
      var(--color-primary-500),
      var(--color-tertiary-500)
    );
    color: var(--color-primary-contrast-500);
    backdrop-filter: blur(16px);
    animation: rotate 2s infinite alternate ease-in-out;
  }

  @property --rotate {
    syntax: "<angle>";
    initial-value: 135deg;
    inherits: false;
  }

  @keyframes rotate {
    from {
      --rotate: 20deg;
    }
    to {
      --rotate: 160deg;
    }
  }
</style>
