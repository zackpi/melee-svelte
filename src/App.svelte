<script lang="ts">
  import "./reset.css";
  import Hud from "./lib/Hud.svelte";
  import Css from "./lib/Css.svelte";
  import Cursor from "./lib/Cursor.svelte";

  let x = 400;
  let y = 400;
  function moveCursor(event: MouseEvent) {
    x = event.clientX;
    y = event.clientY;
  }
</script>

<main on:mousemove={moveCursor}>
  <Hud />
  <Css />
  <Cursor {x} {y} />
</main>

<style>
  :root {
    --darkgray: rgb(20, 20, 20);
  }

  :global(p, h1) {
    font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  }

  main {
    background-color: rgb(20, 16, 36);
    position: relative;
    width: 100%;
    height: 100%;
    overflow: hidden;
    display: flex;
    flex-flow: column;
    gap: 2em;
    align-items: center;
  }
</style>
