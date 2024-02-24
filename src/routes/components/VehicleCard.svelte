<script>
  export let vehicle;

  // Function to handle viewing details or purchasing the vehicle
  const viewDetails = () => {
    // Implement functionality to view details or purchase the vehicle
  };
</script>

<div class="border p-4 m-2">
  <p>{vehicle.make} {vehicle.model} ({vehicle.year})</p>
  <!-- Add additional vehicle details here -->
  <button on:click={viewDetails}>View Details</button>
</div>

<style>
  /* Add styling for the vehicle card */
</style>
