<script>
  import Service from "./Service.svelte";

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
  title={service.title}
  price={service.price}
  on:add-to-cart={addToCart}
  on:delete={deleteService} />
{/each}
