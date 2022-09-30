<script>
	export let name = 'pedro';
	export let initialCounter = 0;
	export let maxCounter = 9;
	let contador = initialCounter;
	
	function handleClick() {
		contador++
	}

	$: isEvenOrOdd = contador % 2 === 0 ? 'Is Even' : 'Is Odd'
	$: name = contador % 2 === 0 ? 'pedro' : 'fer'
	$: if (contador > maxCounter) {
			contador = maxCounter
		}
	
</script>

<main>
	<button on:click={handleClick}>Incrementar</button>
	<p><span>{contador}</span></p>
	<p><span>{isEvenOrOdd}</span></p>
	<h1>Hola {name}!</h1>
	<!-- <p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p> -->
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #175fe4;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	span {
		color: #e47317;
		text-transform: uppercase;
		font-size: 2em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>