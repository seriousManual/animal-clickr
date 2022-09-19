<script lang="ts">
  let what = ''

  let animals = [
    '🐵', '🦓', '🐭', '🐔', '🐨', '🦍', '🐑', '🦊', '🦘', '🐢', '🐠',
    '🦉', '🐧', '🦟', '🐘', '🦕', '🦁', '🐰', '🐪', '🐒', '🐬', '🦆', 
    '🦔'
  ]
</script>

<div class="small">
  {#each animals as animal}
    <button on:click={() => what = animal}>{animal}</button>
  {/each}
</div>

{#if what}
  <div class="big">
    <h1>{what}</h1>

    <button on:click={() => what = ''}>❌</button>
  </div>
{/if}

<style>
  h1 {
    font-size: 10rem;
    font-family: sans-serif;
    text-align: center;
    margin: 0;
  }

  button {
    width: 4rem;
    height: 4rem;
    font-size: 1.5rem;
    margin: 0.2rem;
    background-color: white;
    border: 0.1rem solid;
    border-radius: 0.3rem;
  }

  .small {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    width: 100%;
    margin-bottom: 2rem;
  }

  .big {
    position: relative;
  }

  .big button {
    position: absolute;
    right: 1rem;
    top: 1rem;
    font-size: 2rem;
    border: none;
  }
</style>