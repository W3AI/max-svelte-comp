<script>
  import Service from "./Service.svelte";
  import Modal from './Modal.svelte';

  let services = [
    {
      id: "s1",
      title: "Booking service",
      price: 1.99
    }
  ];

  function addToCart(event) {
    console.log(event.detail);
  }
  function deleteService(event) {
    console.log(event.detail);
  }
</script>

{#each services as service}
<Service
    {...service}
  on:add-to-cart={addToCart}
  on:delete={deleteService} />
{/each}

<Modal content="Servus!" />
