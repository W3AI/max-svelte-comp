<script>
  import Service from "./Service.svelte";
  import Modal from "./Modal.svelte";

  let services = [
    {
      id: "s1",
      title: "Booking service",
      price: 1.99
    }
  ];

  let showModal = false;
  let closeable = false;

  function addToCart(event) {
    console.log(event.detail);
  }
  function deleteService(event) {
    console.log(event.detail);
  }
</script>

{#each services as service}
  <Service {...service} on:add-to-cart={addToCart} on:delete={deleteService} />
{/each}

<button on:click={() => (showModal = true)}>Show Modal</button>

{#if showModal}
  <Modal 
    on:cancel="{() => (showModal = false)}" 
    on:close="{() => (showModal = false)}"
    let:didAgree={closeable}>
    <h1 slot="header">Servus World!</h1>
    <p>innovate as fast as possible!</p>
    <button 
        slot="footer" 
        on:click="{() => (showModal = false)}" 
        disabled={!closeable}
        >Confirm</button>
  </Modal>
{/if}
