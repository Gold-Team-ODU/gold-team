<script>
  import { page } from "$app/state";
  import PageTitle from "./PageTitle.svelte";
</script>

<svelte:head>
  <PageTitle page={page.status.toString()} />
</svelte:head>

<div class="error-container">
  <h1 class="error-status">Uh oh... {page.status}</h1>
  <p>{page.error?.message}</p>
</div>

<style>
  .error-container {
    font-family: "Inter", sans-serif;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 80vh;
    text-align: center;
  }

  .error-status {
    font-family: "Markazi Text", serif;
    font-weight: bolder;
  }

  .error-container h1 {
    font-size: 10rem;
    font-weight: 500;
    margin: 0;
    line-height: 1;
  }

  .error-container p {
    font-size: 1.5rem;
    margin: 1rem 0;
  }
</style>
