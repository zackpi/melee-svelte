<script lang="ts">
  import IconGrid from "./IconGrid.svelte";
  import CardList from "./CardList.svelte";
</script>

<div>
  <IconGrid />
  <CardList />
</div>

<style>
  div {
    display: flex;
    flex-flow: column nowrap;
    gap: 1em;
  }
</style>
