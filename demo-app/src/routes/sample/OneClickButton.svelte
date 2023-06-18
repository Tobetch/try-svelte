<!-- see https://svelte.dev/tutorial/event-modifiers -->
<script>
	function handleClick() {
		alert('no more alerts');
	}
</script>

<!-- <button on:click={handleClick}> Click me </button> -->
<button on:click|once={handleClick}> Click me </button>
