<script lang="ts">
  import IconMoon from "@lucide/svelte/icons/moon";
  import IconSun from "@lucide/svelte/icons/sun";
  import { Switch } from "@skeletonlabs/skeleton-svelte";

  let checked = $state(false);

  $effect(() => {
    const mode = localStorage.getItem("mode") || "light";
    checked = mode === "light";
  });

  const onCheckedChange = (event: { checked: boolean }) => {
    const mode = event.checked ? "light" : "dark";
    document.documentElement.setAttribute("data-mode", mode);
    localStorage.setItem("mode", mode);
    checked = event.checked;
  };
</script>

<svelte:head>
  <script>
    const mode = localStorage.getItem("mode") || "light";
    document.documentElement.setAttribute("data-mode", mode);
  </script>
</svelte:head>

<Switch {checked} {onCheckedChange}>
  {#snippet inactiveChild()}<IconMoon size="14" />{/snippet}
  {#snippet activeChild()}<IconSun size="14" />{/snippet}
</Switch>
