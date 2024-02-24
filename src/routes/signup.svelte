<script>
  import { signup } from "../lib/auth.js";
  import { navigate } from "svelte-routing";

  let email = "";
  let password = "";

  const handleSubmit = async () => {
    try {
      await signup(email, password);
      navigate("/dashboard");
    } catch (error) {
      console.error("Signup failed:", error);
    }
  };
</script>

<h1>Signup</h1>

<form on:submit|preventDefault={handleSubmit}>
  <label for="email">Email:</label>
  <input type="email" id="email" bind:value={email} required />

  <label for="password">Password:</label>
  <input type="password" id="password" bind:value={password} required />

  <button type="submit">Signup</button>
</form>
