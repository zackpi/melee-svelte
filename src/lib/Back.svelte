<script lang="ts">
</script>

<button id="back">
  <div id="wrapper">
    <div>
      <p>BACK</p>
    </div>
  </div>
</button>

<style>
  button {
    --shape: polygon(0 99.5%, 100% 0, 100% 100%, 0.5% 100%);
    position: relative;
    width: 8em;
    height: 4em;
    background-color: transparent;
    border: 0;
  }
  #back div {
    position: absolute;
    left: 0;
    bottom: 0;
    background-color: yellow;
    width: 200em;
    height: 200em;
    clip-path: var(--shape);
  }
  #back div div {
    position: absolute;
    bottom: 0.5em;
    left: 1em;
    background-color: black;
    width: 99%;
    height: 99%;
    clip-path: var(--shape);
  }
  #back div div p {
    position: absolute;
    bottom: 0;
    left: 1em;
    margin: 0;
    font-size: large;
    color: yellow;
    font-weight: bold;
  }
  #back::before {
    position: absolute;
    content: "";
    left: -1.2em;
    bottom: 0;
    z-index: 100;
    background-color: red;
    width: 4.8em;
    height: 2.4em;
    clip-path: polygon(0 60%, 45% 0, 15% 60%, 35% 100%);
  }
</style>
