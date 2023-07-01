<script>
  import { slide } from "svelte/transition";
  import Chevron from "./Chevron.svelte";
  export let title = "Title";
  export let subtitle = "Subtitle";
  export let open = true;
  export let onClick = () => {
    open = !open;
  };
</script>

<section>
<header role="button" on:click="{onClick}">
  <div>
    <h4>{title}</h4>
    <p>{subtitle}</p>
  </div>
  <Chevron {open} {onClick} />
</header>
  {#if open }
    <main transition:slide={{ duration: 500 }}>
      <slot />
    </main>
  {/if}
</section>

<style scoped lang="postcss">
  * {
    margin: 0;
    padding: 0;
  }

  section {
    border-radius: 4px;
  }

  header {
    background: #3468fc;
    border: 0;
    outline: none;
    color: aliceblue;
    padding: 20px;
    cursor: pointer;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  header div {
    text-align: start;
    padding-right: 10px;
  }

  header p {
    margin-top: 8px;
  }

  main {
    text-align: start;
    background: rgb(255, 255, 255);
    padding: 10px;
    border: 0.5px solid #3468fc;
    /* box-shadow: 0 0.125rem 0.25rem rgba(0, 0, 0, 0.075); */
  }
</style>