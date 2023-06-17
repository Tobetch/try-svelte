<!-- https://svelte.dev/tutorial/updating-arrays-and-objects -->
<script>
	let count = 0;

	function handleClick() {
		count += 1;
	}

	let numbers = [1, 2, 3, 4];

	function addNumber() {
		// numbers = [...numbers, numbers.length + 1];
		numbers[numbers.length] = numbers.length + 1;
	}
	$: sum = numbers.reduce((t, n) => t + n, 0);
</script>

<section>
	<button on:click={handleClick}>
		Clicked {count}
		{count === 1 ? 'time' : 'times'}
	</button>

	<div>
		<p>{numbers.join(' + ')} = {sum}</p>

		<button on:click={addNumber}> Add a number </button>
	</div>
</section>
