<script>
  import Service from "./Service.svelte";
</script>

<Service
  serviceTitle="A Booking"
  on:add-to-cart={() => alert('Add to cart!')}
  on:delete={() => {
    alert('Delete!');
  }} />
