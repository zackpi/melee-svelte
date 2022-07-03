<script lang="ts">
  export let src: string;
  export let name: string;
</script>

<button>
  <img {src} alt="doctor mario" />
  <p>{name}</p>
</button>

<style>
  button {
    width: 4em;
    border: 0.1em solid lightgray;
    border-radius: 0.3em;
    overflow: hidden;
    display: flex;
    flex-flow: column;
    padding: 0;
    transition: transform 100ms;
  }

  button:hover {
    transform: scale(1.05);
  }

  img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  p {
    background: linear-gradient(to bottom, black, rgb(80, 0, 0));
    color: lightgray;
    width: 100%;
    font-size: 8pt;
  }
</style>
