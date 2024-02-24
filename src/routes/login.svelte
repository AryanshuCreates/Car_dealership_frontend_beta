<script>
  import { login } from "../lib/auth.js";
  import { navigate } from "svelte-routing";

  let email = "";
  let password = "";

  const handleSubmit = async () => {
    try {
      await login(email, password);
      navigate("/dashboard");
    } catch (error) {
      console.error("Login failed:", error);
    }
  };
</script>

<h1>Login</h1>

<form on:submit|preventDefault={handleSubmit}>
  <label for="email">Email:</label>
  <input type="email" id="email" bind:value={email} required />

  <label for="password">Password:</label>
  <input type="password" id="password" bind:value={password} required />

  <button type="submit">Login</button>
</form>
