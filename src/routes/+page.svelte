<!-- src/routes/+page.svelte -->
<script lang="ts">
  import { supabase } from "$lib/supabaseClient";

  async function signIn() {
    const { data, error } = await supabase.auth.signInWithOAuth({
      provider: "google",
    });
  }
</script>

<h1>Welcome</h1>

<button on:click={signIn}>Sign In</button>
