<script lang="ts">
  let count = $state(0)
  let factor = $state(0)
  let result = $derived(count * factor)
</script>

<main>
  <h1>{count} * {factor} = {result}</h1>
  <div class="row">
    <button onclick={() => count++ }>Count: {count}</button>
    <button onclick={() => factor++ }>Factor: {factor}</button>
  </div>
</main>
<style>
  h1 {
    font-size: 4rem;
    margin: 20px 0;
  }

  button {
    border-radius: 20px;
    font-size: 1.5rem;
    padding: 0.5em 1em;
    cursor: pointer;
  }
</style>