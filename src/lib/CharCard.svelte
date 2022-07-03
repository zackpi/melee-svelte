<script lang="ts">
  export let color: string;

  type PlayerType = "HMN" | "CPU" | "";
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
    return t === "HMN" ? "gold" : t === "CPU" ? "gray" : "rgb(20, 20, 20)";
  }
</script>

<div style:background-color={color}>
  <button
    type="button"
    on:click={togglePlayerType}
    style:border-color={typeColor(type)}
    style:color={typeColor(type)}
  >
    <p>{type}</p>
  </button>
  <input id="hmn" type="text" value="Mario" />
</div>

<style>
  div {
    position: relative;
    width: 10em;
    height: 20em;
    border: 0.24em solid lightgray;
    border-radius: 0.24em;
  }

  button {
    position: absolute;
    top: -0.6em;
    left: -0.6em;
    width: 4em;
    height: 2em;
    border: 0.3em solid rgb(20, 20, 20);
    background-color: rgba(0, 0, 0, 0.8);
    font-weight: bold;
    padding: 0;
  }

  input {
    position: absolute;
    width: 80%;
    left: 10%;
    bottom: 10%;
    border: 0.2em solid gray;
    background-color: rgba(0, 0, 0, 0.8);
    color: white;
    font-family: "Trebuchet MS", "Lucida Sans Unicode", "Lucida Grande",
      "Lucida Sans", Arial, sans-serif;
    font-weight: bold;
    font-size: 16pt;
    padding: 0;
    line-height: 1;
    text-align: center;
  }
</style>
