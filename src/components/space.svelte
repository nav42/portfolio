<!-- components/Space.svelte -->
<script>
  import { onMount } from 'svelte';
  import { Application } from '@splinetool/runtime';

  export let url;
  let canvas;

  onMount(() => {
    const script = document.createElement('script');
    script.src = 'https://unpkg.com/@splinetool/viewer@0.9.381/build/spline-viewer.js';
    script.onload = () => {
      const app = new Application(canvas);
      app.load(url);
    };
    document.head.appendChild(script);
  });
</script>

<canvas bind:this={canvas}></canvas>

<style>
  :global(body) {
    margin: 0;
    overflow: hidden;
  }

  canvas {
    width: 100vw;
    height: 100vh;
    display: block;
    margin: 0;
    padding: 0;
    box-sizing: border-box; 
  }
</style>



