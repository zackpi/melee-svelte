<script lang="ts">
  import CharCard from "./CharCard.svelte";
</script>

<ul>
  <li><CharCard color="#f04040" /></li>
  <li><CharCard color="#4040f0" /></li>
  <li><CharCard color="#f0c040" /></li>
  <li><CharCard color="#40d060" /></li>
</ul>

<style>
  ul {
    border: 1px solid red;
    list-style: none;
    display: flex;
    gap: 1em;
    justify-content: center;
    padding: 0;
  }
</style>
