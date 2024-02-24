<script>
  // Add any necessary imports here

  // Sample data for demonstration
  let vehicles = [
    { id: 1, make: "Toyota", model: "Camry", year: 2022 },
    { id: 2, make: "Honda", model: "Civic", year: 2021 },
    { id: 3, make: "Ford", model: "Fusion", year: 2020 },
  ];
</script>

<h1>Client Dashboard</h1>

<!-- Display list of available vehicles -->
<h2>Available Vehicles</h2>
<ul>
  {#each vehicles as vehicle}
    <li key={vehicle.id}>
      <p>{vehicle.make} {vehicle.model} ({vehicle.year})</p>
      <!-- Add button to view details or purchase vehicle -->
    </li>
  {/each}
</ul>

<!-- Add additional client-specific content here -->
