<!-- routes/+page.svelte -->
<script>
  import Space from "../components/Space.svelte";
  import Header from "../components/Header.svelte";
</script>

<Header />
<div class="space-container">
  <Space url='https://prod.spline.design/uS6VcJEWnW9yqohD/scene.splinecode'/>
</div>  

<style>
  .space-container {
    position: relative;
    width: 100vw;
    height: 100vh;
    margin: 0;
    overflow: hidden;
  }
</style>


