<script lang="ts">
  export let src: string;
  export let name: string;
</script>

<button>
  <div>
    <img {src} alt="doctor mario" />
    <p>{name}</p>
  </div>
</button>

<style>
  button {
    --shape: polygon(
      5% 0,
      95% 0,
      100% 5%,
      100% 95%,
      95% 100%,
      5% 100%,
      0 95%,
      0 5%
    );
    clip-path: var(--shape);
    position: relative;
    width: 4em;
    height: 4.4em;
    border: 0.1em solid lightgray;
    overflow: hidden;
    display: flex;
    flex-flow: column;
    padding: 0;
    transition: transform 100ms;
  }
  button:hover {
    transform: scale(1.05);
  }

  div {
    background: linear-gradient(to bottom, rgb(50, 60, 80), rgb(100, 120, 170));
    clip-path: var(--shape);
    width: 100%;
    height: 100%;
  }

  img {
    clip-path: var(--shape);
    width: 100%;
    height: 100%;
    object-fit: cover;
    filter: drop-shadow(-0.2em 0.4em 0.4em rgba(0, 0, 0, 0.6))
      drop-shadow(0.2em 0.4em 0.4em rgba(0, 0, 0, 0.2));
  }

  p {
    position: absolute;
    bottom: 0;
    left: 0;
    background: linear-gradient(to bottom, black, rgb(80, 0, 0));
    color: lightgray;
    width: 100%;
    font-size: 8pt;
  }
</style>
