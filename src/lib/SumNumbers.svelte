<script>
    let numbers = [1, 2, 3, 4]
    $: sum = numbers.reduce((a, b) => a + b);

    const addNumber = () => {


      numbers = [...numbers, numbers.length + 1];
    }
</script>

<div class="wrapper">
    <div>
    {numbers.join(' + ')} = {sum}
    </div>
    <br/>

    <button on:click={addNumber}>Add a number</button>
    <br/>
    <br/>
</div>

<style>
    .wrapper {
        max-width: 50%;
        margin: auto;
    }
</style>
