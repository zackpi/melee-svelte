<script lang="ts">
  import src from "../assets/pointing.png";
  export let x: number;
  export let y: number;
</script>

<img {src} alt="cursor" style:left={`${x}px`} style:top={`${y}px`} />

<style>
  :global(*) {
    cursor: none;
  }

  img {
    position: absolute;
    z-index: 1000;
    top: 0;
    left: 0;
    width: 6em;
    height: 6em;
    margin-left: -1.6em;
    margin-top: -1.6em;
    pointer-events: none;
    filter: drop-shadow(1px 3px 2px rgba(0, 0, 0, 0.5))
      drop-shadow(5px 8px 5px rgba(0, 0, 0, 0.3));
  }
</style>
