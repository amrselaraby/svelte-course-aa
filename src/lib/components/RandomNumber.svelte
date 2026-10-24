<script lang="ts">
	import { untrack } from 'svelte';

	let randomNumber = $state(Math.floor(Math.random() * 10));
	let history: number[] = $state([]);
	$effect(() => {
		untrack(() => {
			history.push(randomNumber);
		});
	});
</script>

<h2>This is random number: {randomNumber}</h2>
<button
	onclick={() => {
		randomNumber = Math.floor(Math.random() * 10);
	}}>Generate</button
>
