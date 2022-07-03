<script lang="ts">
  import Vs from "./Vs.svelte";
  import Settings from "./Settings.svelte";
  import Back from "./Back.svelte";
</script>

<div id="hud">
  <div id="title">
    <h1>MELEE</h1>
    <Vs />
  </div>
  <Settings />
  <Back />
</div>

<style>
  #hud {
    position: relative;
    width: 100%;
    display: flex;
    justify-content: center;
    gap: 3em;
    align-items: center;
    padding-top: 1.4em;
  }

  #title {
    position: relative;
    display: flex;
    align-items: center;
    gap: 1em;
    height: 100%;
  }

  #title * {
    z-index: 10;
  }

  #title:before {
    content: "";
    position: absolute;
    bottom: -0.4em;
    right: -100em;
    z-index: 0;
    clip-path: polygon(0 0, 100% 0, 100% 6em, 102.4em 6em, 100em 100%, 0 100%);
    background-color: rgba(80, 90, 100, 0.7);
    width: 200em;
    height: 10em;
  }

  h1 {
    color: var(--darkgray);
    font-style: italic;
  }
</style>
