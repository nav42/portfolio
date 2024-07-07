<!-- components/header.svelte-->
<script>
  import { page } from "$app/stores";

  let current_path;
  function rstrip(text, pattern) {
    let regex = new RegExp(pattern + "$");
    return text.replace(regex, "");
  }

  function lstrip(text, pattern) {
    let regex = new RegExp("^" + pattern);
    return text.replace(regex, "");
  }

  function strip(text, pattern) {
    let r = rstrip(text, pattern);
    return lstrip(r, pattern);
  }
  $: current_path = strip($page.url.pathname, "/");
</script>

<header>
  <nav>
    <a
      aria-current={current_path.startsWith("yo") ? "page" : undefined}
      href="/yo">yo</a
    >
    <a
      aria-current={current_path.startsWith("yo2") ? "page" : undefined}
      href="/yo2">yo2</a
    >
  </nav>
</header>

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
