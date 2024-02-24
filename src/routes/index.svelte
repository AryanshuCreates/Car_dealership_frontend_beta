<script>
  import { onMount } from "svelte";
  import { navigate } from "svelte-routing";

  // Mock data for demonstration purposes
  let vehicles = [
    { id: 1, name: "Vehicle 1", description: "Description for Vehicle 1" },
    { id: 2, name: "Vehicle 2", description: "Description for Vehicle 2" },
    { id: 3, name: "Vehicle 3", description: "Description for Vehicle 3" },
  ];

  const viewVehicleDetails = (vehicleId) => {
    navigate(`/vehicle/${vehicleId}`);
  };
</script>

<h1>Welcome to Car Dealership</h1>

<div>
  <h2>Available Vehicles</h2>
  {#each vehicles as vehicle}
    <div on:click={() => viewVehicleDetails(vehicle.id)}>
      <p>{vehicle.name}</p>
      <p>{vehicle.description}</p>
    </div>
  {/each}
</div>
