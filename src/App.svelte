<script>
  import BasicMultiplier from "./lib/BasicMultiplier.svelte";
  import CarSearch from "./lib/CarSearch.svelte";

  let components = [ BasicMultiplier, CarSearch ];
  let current = $state(0);
  let Component = $derived(components[current]);

</script>
<Component />
<div class="components-changer">
  <button onclick={() => current = (current - 1 + components.length) % components.length}>&lt;</button>
  <button onclick={() => current = (current + 1) % components.length}>&gt;</button>
</div>

<style>
  .components-changer {
    display: flex;
    position: fixed;
    justify-content: space-between;
    bottom: 20px;
    margin-top: 2rem;
    padding: 0 20px ;
    width: 100%;
  }

  button {
    border-radius: 10px;
    padding: 0.5rem 1rem;
    font-size: 2rem;
    cursor: pointer;
    font-weight: 800;
    margin: 0 20px;
  }
</style>