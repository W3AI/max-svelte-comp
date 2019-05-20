<script>
  import Service from "./Service.svelte";

  function addToCart(event) {
      console.log(event.detail);
  }
    function deleteService(event) {
      console.log(event.detail);
  }
</script>

<Service
  serviceTitle="A Booking"
  on:add-to-cart={addToCart}
  on:delete={deleteService} />
