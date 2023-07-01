<script>
 export let buttonType = "primary";
 export let outlined = false;
 export let disabled = false;
 export let buttonText = "Button Text";
</script>

<style>
	button {
	  border: none;
	  padding: 8px 12px;
	  border-radius: 2px;
	  cursor: pointer;
	}

	.link {
	  background: none;
	  color: #3468fc;
	}

	.primary {
	  background: #3468fc;
	  color: #ffffff;
	}

	.primary.outlined {
	  background: none;
	  color: #3468fc;
	  border: 1px solid #3468fc !important;
	}

	.primary.disabled {
	  pointer-events: none;
	  background-color: whitesmoke;
	  color: lightgrey;
	}

	.secondary {
	  background: #ffffff;
	  color: #3468fc;
	}
</style>

<button 
	on:click
	class={buttonType} 
	class:outlined={outlined} 
	class:disabled={disabled}
>
  <slot> {buttonText} </slot>
</button>