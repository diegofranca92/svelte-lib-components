<script>
	import CloseIcon from "./Icons/Close.svelte";
	import Button from "./shared/components/Button.svelte";

	function handleClick() {
	  alert("Button Clicked");
	}
</script>

<style>
	header {
	  display: flex;
	  justify-content: space-between;
	  align-items: center;
	  padding: 4px;
	  border-bottom: 1px solid #cecece;
	}
</style>

<header>
	<h4>CANCELAMENTO ESPECIAL</h4>
	<Button 
		on:click
		buttonType="link"
		buttonText={"X"} 
	/>
</header>
<main>
	<p>
		Faça um upgrade na sua reserva e tenha seu dinheiro de volta caso precise cancelar. Por apenas R$ 200,00 garanta o
		seu reembolso total, ver mais.
	</p>
</main>
<Button 
	on:click={handleClick}
	buttonType="primary" 
	outlined={true} 
	buttonText="Não, obrigado" 
/>
<Button 
	buttonType="primary" 
	buttonText="Adicionar à reserva" 
/>