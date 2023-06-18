<!-- https://svelte.dev/tutorial/updating-arrays-and-objects -->
<script>
	import CountNumber from './CountNumber.svelte';
	import AddNumber from './AddNumber.svelte';
	import Nested from './Nested.svelte';
	import Info from './Info.svelte';
	import ToggleButton from './ToggleButton.svelte';

	const pkg = {
		name: 'svelte',
		version: 3,
		speed: 'blazing',
		website: 'https://svelte.dev'
	};
</script>

<section>
	<CountNumber />
	<hr />

	<AddNumber />
	<hr />

	<Nested answer={42} />
	<hr />

	<!-- Spread props -->
	<!-- <Info name={pkg.name} version={pkg.version} speed={pkg.speed} website={pkg.website} /> -->
	<Info {...pkg} />
	<hr />

	<ToggleButton />
</section>
