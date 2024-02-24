<script>
  // Add any necessary imports here

  // Sample data for demonstration
  let dealerships = [
    { id: 1, name: "ABC Motors" },
    { id: 2, name: "XYZ Cars" },
    // Add more dealership data as needed
  ];
</script>

<div class="sidebar">
  <h2>Dealerships</h2>
  <ul>
    {#each dealerships as dealership}
      <li key={dealership.id}>{dealership.name}</li>
    {/each}
  </ul>
</div>

<style>
  /* Add styling for the sidebar */
</style>
