<script lang="ts">
  import src from "../assets/svelte.png";
  import CharIcon from "./CharIcon.svelte";
</script>

<div>
  <ul>
    <li><CharIcon {src} name="Dr. MARIO" /></li>
    <li><CharIcon {src} name="Dr. MARIO" /></li>
    <li><CharIcon {src} name="Dr. MARIO" /></li>
    <li><CharIcon {src} name="Dr. MARIO" /></li>
    <li><CharIcon {src} name="Dr. MARIO" /></li>
    <li><CharIcon {src} name="Dr. MARIO" /></li>
    <li><CharIcon {src} name="Dr. MARIO" /></li>
    <li><CharIcon {src} name="Dr. MARIO" /></li>
    <li><CharIcon {src} name="Dr. MARIO" /></li>
  </ul>
  <ul>
    <li><CharIcon {src} name="Dr. MARIO" /></li>
    <li><CharIcon {src} name="Dr. MARIO" /></li>
    <li><CharIcon {src} name="Dr. MARIO" /></li>
    <li><CharIcon {src} name="Dr. MARIO" /></li>
    <li><CharIcon {src} name="Dr. MARIO" /></li>
    <li><CharIcon {src} name="Dr. MARIO" /></li>
    <li><CharIcon {src} name="Dr. MARIO" /></li>
    <li><CharIcon {src} name="Dr. MARIO" /></li>
    <li><CharIcon {src} name="Dr. MARIO" /></li>
  </ul>
  <ul>
    <li><CharIcon {src} name="Dr. MARIO" /></li>
    <li><CharIcon {src} name="Dr. MARIO" /></li>
    <li><CharIcon {src} name="Dr. MARIO" /></li>
    <li><CharIcon {src} name="Dr. MARIO" /></li>
    <li><CharIcon {src} name="Dr. MARIO" /></li>
    <li><CharIcon {src} name="Dr. MARIO" /></li>
    <li><CharIcon {src} name="Dr. MARIO" /></li>
  </ul>
</div>

<style>
  div {
    z-index: 100;
    display: flex;
    flex-flow: column;
    gap: 0.2em;
    margin: 0;
  }

  ul {
    list-style-type: none;
    display: flex;
    gap: 0.2em;
    justify-content: center;
    padding: 0;
  }

  li:first-child {
    margin-top: 0.4em;
  }

  li:last-child {
    margin-top: 0.4em;
  }
</style>
