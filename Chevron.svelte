<script>
  export let open = false;
  export let onClick = () => {
    open = !open;
  };
</script>

<svg class:open on:click="{onClick}" xmlns="http://www.w3.org/2000/svg" width="15" height="15" viewBox="0 0 15 10" fill="none">
  <path d="M8.29453 0.488274L14.6695 6.86328C15.1102 7.30391 15.1102 8.01641 14.6695 8.45235L13.6102 9.51172C13.1695 9.95235 12.457 9.95235 12.0211 9.51172L7.50234 4.99297L2.98359 9.51173C2.54297 9.95235 1.83047 9.95235 1.39453 9.51173L0.335156 8.45235C-0.105469 8.01172 -0.105469 7.29922 0.335156 6.86328L6.71015 0.488275C7.1414 0.0476488 7.8539 0.0476488 8.29453 0.488274V0.488274Z" fill="white"/>
</svg>

<style lang="scss" scoped>
  svg {
    transition: transform 500ms;
  }

  .open {
    transform: rotate(180deg);
  }
</style>