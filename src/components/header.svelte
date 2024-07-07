<!-- components/header.svelte-->
<script>
</script>

<style>
  header {
    width: 100%;
    height: 60px;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 0 20px;
    background-color: #333;
    color: white;
    position: absolute;
    top: 0;
    left: 0;
    z-index: 10;
  }

  nav {
    display: flex;
    align-items: center;
  }

  nav a {
    color: white;
    text-decoration: none;
    margin-left: 20px;
    font-size: 20px;
  }

  nav a:hover {
    text-decoration: underline;
  }
</style>

<header>
  <nav>
    <a href="/yo">yo</a>
    <a href="/yo2">yo2</a>
  </nav>
</header>

