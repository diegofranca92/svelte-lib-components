<script>
export let modalContent;
</script>

<main on:click|self class="modal">
  <div class="content">
    <svelte:component on:click this={modalContent} />
  </div>
</main>

<style>
	.modal {
	  background-color: rgba(0, 0, 0, 0.4);
	  position: absolute;
	  top: 0;
	  left: 0;
	  width: 100%;
	  height: 100%;
	  display: flex;
	  justify-content: center;
	  align-items: center;
	}

	.content {
	  background-color: white;
	  width: 20em;
	  height: 15em;
	}
</style>