<script lang="ts">
    let car = $state('');
    let logo = $state('');

    $effect(() => {
        logo = `../../images/${car}.png`
    })
</script>

<div>
    <p>Search: BMW, Audi, Porsche or Toyota</p>
    <input
        type="search"
        placeholder="Search cars"
        oninput={ e => car = e.target.value.toLowerCase() }
    />

    <img src={logo} alt={car} />
</div>

<style>
    div {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 1rem;
    }
    
    img {
        margin-top: 20px;
        width: auto;
        height: 150px;
    }
</style>