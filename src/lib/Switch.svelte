<script lang="ts">
    let isOn = $state(false);

    $effect(() => {
        const circle = document.querySelector('.circle') as HTMLElement;
        if (isOn) {
            circle.style.left = '65px';
            circle.style.backgroundColor = 'limegreen';
        } else {
            circle.style.left = '5px';
            circle.style.backgroundColor = 'orangered';
        }
    });
</script>

<main>
    <div class="switch" onclick={() => isOn = !isOn}>
        <div class="circle"></div>
    </div>
</main>

<style>
    .switch {
        width: 120px;
        height: 60px;
        background-color: #ccc;
        border-radius: 30px;
        position: relative;
        cursor: pointer;
    }

    .circle {
        width: 50px;
        height: 50px;
        background-color: orangered;
        border-radius: 50%;
        position: absolute;
        top: 5px;
        left: 5px;
        transition: left 0.3s;
    }
</style>