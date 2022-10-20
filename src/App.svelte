<script>
  import Counter from "./lib/Counter.svelte";
</script>

<main>
  <div class="contianer"><h1>Marwan Alsouki</h1></div>

  <img src="./vite.svg" class="logo" alt="Vite Logo" />

  <img src="./svelte.svg" class="logo svelte" alt="Svelte Logo" />

  <h1>Vite + Svelte</h1>

  <div class="card">
    <Counter />
  </div>
</main>

<style>
  .contianer {
    position: relative;
    cursor: pointer;
    color: aquamarine;
    transition: 0.2s;
  }
  .contianer:hover {
    filter: drop-shadow(0 0 2em aquamarine);
    transform: scale(1.1);
  }
  .contianer::after {
    position: absolute;
    left: -10px;
    top: 1px;
    content: "";
    width: 6px;
    height: 50px;
    color: red;
    background-color: red;
    transform: translate(0px);
    transition: 1s;
  }
  .contianer:hover::after {
    transform: translate(400px);
  }
  .logo {
    height: 6em;
    padding: 1.5em;
    will-change: filter;
  }
  .logo:hover {
    filter: drop-shadow(0 0 2em #646cffaa);
  }
  .logo.svelte:hover {
    filter: drop-shadow(0 0 2em #ff3e00aa);
  }
</style>
