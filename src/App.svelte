<script>
	import Counter from './Counter.svelte'
	import Input from './Input.svelte'

	const commomProps = { maxCounter: 15 }
</script>


<Input/>
<!-- <Counter initialCounter={2} {...commomProps} /> -->
<Counter initialCounter={3} {...commomProps} />