<script lang="ts">
  type PlayerType = "HMN" | "CPU" | "";

  export let color: string;
  let name = "Mario";
  let type: PlayerType = "";

  function togglePlayerType() {
    if (type === "HMN") type = "CPU";
    else if (type === "CPU") type = "";
    else type = "HMN";
  }
  function setPlayerType(t: PlayerType) {
    type = t;
  }
  function typeColor(t: PlayerType) {
    return t === "HMN" ? "goldenrod" : t === "CPU" ? "gray" : "rgb(70, 70, 80)";
  }
</script>

<div
  id="card"
  style:background-color={type === "HMN"
    ? color
    : type === "CPU"
    ? "rgb(100,100,120)"
    : "rgb(50,50,90)"}
>
  <button
    type="button"
    on:click={togglePlayerType}
    style:background-color={typeColor(type)}
    style:color={typeColor(type)}
  >
    <p>{type}</p>
  </button>

  <div class="hmn">
    {#if type === ""}
      <p />
    {:else}
      <input type="text" bind:value={name} />
    {/if}
  </div>
</div>

<style>
  #card {
    position: relative;
    width: 10em;
    height: 20em;
    border: 0.24em solid lightgray;
    border-radius: 0.24em;
  }
  #card::before {
    content: "";
    position: absolute;
    bottom: 0;
    left: 0;
    width: calc(100% - 0.4em);
    height: calc(100% - 0.4em);
    border: 0 solid rgba(0, 0, 0, 0.2);
    border-width: 0.2em 0.2em 0 0;
    border-top-right-radius: 1.6em;
  }
  #card::after {
    content: "";
    position: absolute;
    bottom: 0;
    left: 0.6em;
    width: calc(100% - 1.8em);
    height: calc(100% - 1.2em);
    background-color: rgba(0, 0, 0, 0.3);
    clip-path: polygon(30% 5%, 40% 0%, 90% 0, 100% 5%, 100% 100%, 0 99%, 0% 5%);
  }

  button {
    --player-type-shape: polygon(75% 0, 100% 30%, 75% 100%, 0 100%, 0 0);
    clip-path: var(--player-type-shape);
    position: absolute;
    z-index: 50;
    top: -0.6em;
    left: -0.6em;
    width: 4em;
    height: 2em;
    border: 0;
    font-weight: bold;
    padding: 0;
    box-shadow: inset -0.1em -0.1em rgba(0, 0, 0, 0.2);
  }
  button::before {
    clip-path: var(--player-type-shape);
    content: "";
    position: absolute;
    top: 0.2em;
    left: 0.4em;
    width: calc(100% - 0.8em);
    height: calc(100% - 0.6em);
    background-color: rgb(20, 30, 40);
  }
  button p {
    position: relative;
    z-index: 100;
    font-size: 14pt;
    filter: drop-shadow(2px 2px black) brightness(1.3);
  }

  .hmn {
    position: absolute;
    z-index: 300;
    width: 80%;
    height: 1.6em;
    left: 10%;
    bottom: 3em;
  }
  .hmn * {
    width: 100%;
    height: 100%;
    border-radius: 0.2em;
    border: 0.2em solid gray;
    background-color: rgba(0, 0, 0, 0.8);
    color: white;
    font-family: "Trebuchet MS", "Lucida Sans Unicode", "Lucida Grande",
      "Lucida Sans", Arial, sans-serif;
    font-weight: bold;
    font-size: 14pt;
    padding: 0;
    line-height: 1;
    text-align: center;
  }
  .hmn::before {
    counter-increment: player;
    content: "P" counter(player);
    position: absolute;
    z-index: -1;
    top: 0.5rem;
    left: -10%;
    width: 120%;
    height: 4rem;
    border: 0.2rem solid rgb(80, 90, 100);
    border-radius: 0.6rem 0.6rem 0 0;
    background-color: rgb(20, 24, 30, 0.7);
    color: gray;
    font-size: 32pt;
    font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
    font-weight: bold;
    font-style: italic;
  }
</style>
