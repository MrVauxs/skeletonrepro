<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

<script lang="ts">
	import { Switch } from '@skeletonlabs/skeleton-svelte';

	// Bind to the checked state
	let mode = $state(false);

	// Handle the change in state when toggled.
	function handleModeChange() {
		// NOTE: implementation may differ per Tailwind config and framework:
		// https://tailwindcss.com/docs/dark-mode#toggling-dark-mode-manually
		console.log({ mode });
	}
</script>

<Switch name="mode" controlActive="bg-surface-200" bind:checked={mode} onchange={handleModeChange}>
	{#snippet inactiveChild()}a{/snippet}
	{#snippet activeChild()}b{/snippet}
</Switch>