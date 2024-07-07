<!-- src/routes/__layout.svelte or src/routes/layout.svelte -->
<script>
  import Header from '../components/header.svelte';
</script>



<main>
  <slot></slot>
</main>

<style global>
  html, main {
    margin: 0;
    padding: 0;
    width: 100%;
    height: 100%;
    overflow: hidden;
    box-sizing: border-box;
  }

  * {
    box-sizing: inherit;
  }
</style>
