<script lang="ts">
  import Customers from "./Customers.svelte";
  import PageTitle from "./PageTitle.svelte";
  import ProblemSolution from "./ProblemSolution.svelte";
</script>

<svelte:head>
  <PageTitle />
</svelte:head>

<div>
  <div class="grid grid-cols-[auto_1fr] p-2">
    <header
      class="h2 px-5 [writing-mode:vertical-lr] rotate-180 place-self-start"
    >
      Our Goal
    </header>
    <article class="text-justify self-center pl-5 text-base xl:text-lg">
      <p>
        We aim to develop a game to help those who struggle to understand
        algebra. Our game will be a single-player, turn-based, rogue-like adventure through
        algebra. With dungeons, bosses, and power-ups all throughout, you'll be
        engaged in the world as much as you are with the math. But be sure to
        calculate your next step carefully. Damage is dealt to the reckless, and
        penalties will be incurred for wrong answers. Find hints and collect
        extra lives to survive your mathematical journey.
      </p>
      <br />
      <p class="italic font-semibold font-serif text-xl text-center">
        “Gamify algebra—turn problem-solving into an adventure!”
      </p>

      <hr class="hr border-t-2 my-5" />

      <ProblemSolution />

      <hr class="hr border-t-2 my-5" />

      <Customers />
    </article>
  </div>
</div>
