<script>
    let counter = 0;
    // reactive variable
    $: doubledCounter = counter * 2;

    const increment = () => {
      counter++;
    }

    const decrement = () => {
      counter--;
    }

    //reactive block
    $: if (counter >= 10) {
      alert('count is dangerously high!');
      counter = 9;
    }
</script>

<div class="block">
    <button class="btn" on:click={decrement}>-</button>
    <p>{counter}</p>
    <button class="btn" on:click={increment}>+</button>

    Doubled counter: {doubledCounter}
</div>

<style>
    .block {
        display: flex;
        gap: 15px;
        justify-content: center;
    }
</style>
