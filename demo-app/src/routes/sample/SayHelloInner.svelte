<script>
	import { createEventDispatcher } from 'svelte';

	const dispatch = createEventDispatcher();

	// メッセージイベント
	function sayHello() {
		dispatch('myevent', {
			text: 'Hello!',
			text2: ',Tobetch!'
		});
	}
</script>

<button on:click={sayHello}> Click to say hello </button>
