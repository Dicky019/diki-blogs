<script>
  import Header from "../components/Header.svelte";
  export let segment;
</script>

<div class="layout">
  <Header {segment} />

  <main>
    <slot />
  </main>

  <footer>
    <span>
      &copy; {new Date().getFullYear()} This Blog. Created by
      <a href="https://www.instagram.com/dicky.219/" target="_blank">Diki</a>
      <!-- . Template
      by
      <a href="https://www.twitter.com/Charca" target="_blank">Maxi Ferreira</a
      >. -->
    </span>
  </footer>
</div>

<style>
  .layout {
    display: flex;
    flex-direction: column;
    min-height: 100%;
    min-height: 100vh;
  }

  main {
    flex: 1;
    position: relative;
    margin: 0 auto;
    max-width: 1400px;
    background-color: white;
    padding: 1em 2em;
    box-sizing: border-box;
    width: 100%;
    display: flex;
    flex-direction: column;
  }

  footer {
    color: #aaa;
    font-size: 1em;
    font-family: Rubik, sans-serif;
    margin: 1em auto;
    max-width: 1400px;
    padding: 1em 2em;
    text-align: center;
    width: 100%;
  }
</style>
