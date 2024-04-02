<script lang="ts">
	export let type: 'filled' | 'tonal' | 'text' | 'outlined';
	export let icon = '';
	export let href = '';
	export let target = '';
	export let label = '';
</script>

{#if href}
	<a {href} {target} class={`button-${type}`} aria-label={label}>
		{#if icon}
			<img src="../{icon}.ico" alt={icon} />
		{/if}
		<slot />
	</a>
{:else}
	<button on:click class={`button-${type}`} aria-label={label}>
		{#if icon}
			<img src="../{icon}.ico" alt={icon} />
		{/if}
		<slot />
	</button>
{/if}
