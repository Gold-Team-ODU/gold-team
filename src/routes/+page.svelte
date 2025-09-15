<script lang="ts">
  import { Tabs } from "@skeletonlabs/skeleton-svelte";
  import PageTitle from "./PageTitle.svelte";
  import Placeholder from "./Placeholder.svelte";

  let group = $state("problem");
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
        algebra. Our game will be a turn-based, rogue-like adventure through
        algebra. With dungeons, bosses, and power-ups all throughout, you'll be
        engaged in the world as much as you are with the math. But be sure to
        calculate your next step carefully. Damage is dealt to the reckless, and
        penalties will be incurred for wrong answers. Find hints and collect
        extra lives to survive your mathematical journey.
      </p>
      <br />
      <p class="italic font-semibold font-serif">
        “Gamify algebra—turn problem-solving into an adventure!”
      </p>

      <hr class="hr border-t-2 my-5" />

      <div
        class="card preset-filled-surface-50-950 border-surface-200-800 divide-surface-200-800 block divide-y overflow-hidden"
      >
        <Tabs value={group} onValueChange={(e) => (group = e.value)} fluid>
          {#snippet list()}
            <Tabs.Control value="problem"
              ><header class="h3">Problem</header></Tabs.Control
            >
            <Tabs.Control value="solution"
              ><header class="h3">Solution</header></Tabs.Control
            >
          {/snippet}
          {#snippet content()}
            <div class="accent-error-50-950">
              <Tabs.Panel value="problem">
                <article class="text-justify text-lg p-5">
                  <p>
                    <span class="font-bold">Algebra</span>, while being a very
                    useful skill for daily life and forming the backbone of
                    mathematics, is
                    <span class="font-bold">extremely difficult</span> for the average
                    person to understand.
                  </p>
                </article>
              </Tabs.Panel>
            </div>
            <Tabs.Panel value="solution">
              <article class="text-justify text-lg p-5">
                <p>
                  A <span class="font-bold"
                    >solo, turn-based, rogue-like game</span
                  >
                  where the player adventures through dungeons, tackling enemies
                  and increasing in power and algebraic knowledge as they adventure
                  along.
                </p>
              </article>
            </Tabs.Panel>
          {/snippet}
        </Tabs>
      </div>

      <hr class="hr border-t-2 my-5" />

      <div class="grid grid-cols-1 md:grid-cols-2 gap-2">
        <div
          class="card preset-filled-surface-50-950 border-[3px] border-surface-200-800 divide-surface-200-800 block divide-y overflow-hidden space-y-4 p-4"
        >
          <header class="h3"><p>Customers</p></header>
          <article>
            <ul class="list-inside list-disc space-y-2">
              <li>Schools and tutoring centers</li>
              <li>Parents who want to help their kids learn math</li>
              <li>Self-learners improving their algebra skills</li>
              <li>Libraries and Community learning programs</li>
              <li>Companies for employee training</li>
            </ul>
          </article>
        </div>
        <div
          class="card preset-filled-surface-50-950 border-[3px] border-surface-200-800 divide-surface-200-800 block divide-y overflow-hidden space-y-4 p-4"
        >
          <header class="h3"><p>End Users</p></header>
          <article>
            <ul class="list-inside list-disc space-y-2">
              <li>Middle and high school students</li>
              <li>College students needing extra math practice</li>
              <li>Gamers who enjoy strategy games</li>
              <li>STEM learners and aspiring programmers</li>
              <li>Adults wanting to improve their math skills</li>
            </ul>
          </article>
        </div>
      </div>
    </article>
  </div>
</div>

<style>
</style>
