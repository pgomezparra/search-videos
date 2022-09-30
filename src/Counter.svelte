<script>
	export let name = 'pedro';
	export let initialCounter = 0;
	export let maxCounter = 9;
	let contador = initialCounter;
	
	function handleClick() {
		name = 'Fer'
		contador++
	}

	$: isEvenOrOdd = contador % 2 === 0 ? 'Is Even' : 'Is Odd'
	$: if (contador > maxCounter) {
			contador = maxCounter
		}
	
</script>

<main>
	<button on:click={handleClick}>Incrementar</button>
	<span>{contador}</span>
	<h1>Hola {name}!</h1>
	<!-- <p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p> -->
	<span>{isEvenOrOdd}</span>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1, span {
		color: #175fe4;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>