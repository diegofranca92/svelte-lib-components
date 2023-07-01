<script>
  import "./global.css";
  import Accordion from "./Accordion.svelte";
  import Modal from "./Modal.svelte";
  import CancelationModal from "./CancelationModal.svelte";

  export let list = [
    "COVID-19 infecção e isolamento",
    "Doença, Acidente, Lesão",
    "Condição médica pré-existente",
    "Roubo de documentos",
    "Falha com veículo privado",
    "E muito mais..."
  ];

  let showModal = false;
  let modalContent;

  function toogleModal(component) {
    showModal = !showModal;
    modalContent = component;
  }
</script>

<style>
  main {
    font-family: sans-serif;
    text-align: center;
  }
</style>

<main>
  <Accordion
    title="CANCELAMENTO ESPECIAL" 
    subtitle="Escolha o seu quarto e adicione o cancelamento especial na próxima etapa. Saiba mais. ">
    <div>
      <h4>Entenda os seus termos de reembolso</h4>
      <ul>
        {#each list as item}
          <li>{item}</li>
        {/each}
      </ul>
      <button
        on:click={() => toogleModal(CancelationModal)}>
        Ver menos
      </button>
      <p>Faça um upgrade na sua reserva e tenha seu dinheiro de volta caso precise cancelar. </p>
      <a href="#">Confira as condições</a>
    </div>
  </Accordion>
  {#if showModal}
    <Modal role="dialog" on:click={toogleModal} {modalContent} />
  {/if}
</main>