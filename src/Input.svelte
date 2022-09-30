<script>
    let value = ''

    const handleInput = (event) => 
        value = event.target.value
</script>

<input value={value} on:input={handleInput} />