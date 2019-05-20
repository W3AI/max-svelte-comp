<script>
  import Service from "./Service.svelte";

  function addToCart(event) {
      console.log(event);
  }
    function deleteService(event) {
      console.log(event);
  }
</script>

<Service
  serviceTitle="A Booking"
  on:add-to-cart={addToCart}
  on:delete={deleteService} />
