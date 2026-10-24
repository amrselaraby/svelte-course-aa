<script lang="ts">
	import Button from '#lib/components/Button.svelte';
	import { AlarmClockCheck, Search } from '@lucide/svelte';
</script>

<Button size="sm" shadow>
	{#snippet left(isHovered: boolean)}
		{#if isHovered}
			<Search />
		{:else}
			<AlarmClockCheck />
		{/if}
	{/snippet}
	text
	{#snippet right()}
		<AlarmClockCheck />
	{/snippet}
</Button>
