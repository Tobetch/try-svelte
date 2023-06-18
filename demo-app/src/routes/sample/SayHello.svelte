<script>
	import SayHelloInner from './SayHelloInner.svelte';

	function handleMessage(event) {
		const { text, text2 } = event.detail;
		alert(text + text2);
	}
</script>

<SayHelloInner on:myevent={handleMessage} />
