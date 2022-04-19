<script>
  export let name;
  import LoadingFadeout from "./LoadingFadeout.svelte";
  import Nested from "./Nested.svelte";
  import { fly, fade } from "svelte/transition";
</script>

<main>
  <LoadingFadeout>
    <div in:fly={{ y: 200, duration: 2000 }} out:fade>
      <h1>Hello {name}!</h1>
      <p>
        Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn
        how to build Svelte apps.
      </p>
      <p>This is a paragraph.</p>
      <Nested />
    </div>
  </LoadingFadeout>
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
    background-color: #0df4d2;
    position: relative;
    width: 100%;
    min-height: 100vh;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }

  p {
    color: purple;
    font-family: "Comic Sans MS", cursive;
    font-size: 2em;
  }
</style>
