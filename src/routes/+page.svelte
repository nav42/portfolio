<script>
  let count = 0;
</script>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

<h1> NAV : {count}</h1>
<button on:click={() => count += 1}>Increment</button>
<button on:click={() => count -= 1}>Decrement</button>

