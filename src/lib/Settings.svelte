<div>
  <p>4-man survival test!</p>
</div>

<style>
  div {
    --shape: polygon(4% 0%, 98% 0%, 100% 50%, 96% 100%, 2% 100%, 0% 50%);
    clip-path: var(--shape);
    position: relative;
    padding: 0.8em 2em 0.8em 2em;
    transition: transform 100ms;
  }
  div:hover {
    transform: scale(1.05);
  }
  div::before {
    position: absolute;
    background-color: gray;
    content: "";
    top: 0.6em;
    left: 0.6em;
    width: calc(100% - 1.2em);
    height: calc(100% - 1.2em);
    clip-path: var(--shape);
  }

  div p {
    width: 100%;
    height: 100%;
    clip-path: var(--shape);
    background-color: black;
    padding: 0 2em 0 2em;
    color: white;
    font-weight: bold;
  }
</style>
