<script lang="ts">
</script>

<button>
  <div>
    <div>
      <p>BACK</p>
    </div>
  </div>
</button>

<style>
  button {
    --shape: polygon(0 99.5%, 100% 0, 100% 100%, 0.5% 100%);
    position: relative;
    z-index: 200;
    background-color: transparent;
    border: 0;
    margin: 2em 2em 0 0;
    transition: transform 100ms;
  }
  button:hover {
    transform: translateX(-1em) translateY(1em);
  }
  button::before {
    position: absolute;
    content: "";
    left: -1.2em;
    bottom: 0;
    z-index: -1;
    background-color: red;
    width: 4.8em;
    height: 2.4em;
    clip-path: polygon(0 60%, 45% 0, 15% 60%, 35% 100%);
    pointer-events: none;
    animation: none;
  }
  button:hover::before {
    animation: flash 1s linear infinite;
  }

  button div {
    position: absolute;
    left: 0;
    bottom: 0;
    background-color: yellow;
    width: 200em;
    height: 200em;
    clip-path: var(--shape);
  }
  button div div {
    position: absolute;
    bottom: 0.5em;
    left: 1em;
    background-color: black;
    width: 99%;
    height: 99%;
    clip-path: var(--shape);
  }
  button div div p {
    position: absolute;
    bottom: 0;
    left: 1em;
    margin: 0;
    font-size: large;
    color: yellow;
    font-weight: bold;
  }

  @keyframes flash {
    0% {
      left: -1.2em;
      opacity: 100%;
    }
    25% {
      left: -1.5em;
      opacity: 50%;
    }
    50% {
      left: -1.8em;
      opacity: 0;
    }
    51% {
      left: -0.6em;
      opacity: 0;
    }
    75% {
      left: -0.9em;
      opacity: 100;
    }
    100% {
      left: -1.2em;
      opacity: 100%;
    }
  }
</style>
