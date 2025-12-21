<script lang="ts">
	import type { Snippet } from 'svelte';

	type Props = {
		title?: string;
		children: Snippet;
	};

	let { title, children }: Props = $props();
</script>

<div class="space-y-2">
	{#if title}
		<h3 class="font-semibold">{title}</h3>
	{/if}
	<ul class="space-y-2">
		{@render children()}
	</ul>
</div>
