<script lang="ts">
	import type { Snippet } from 'svelte';
	import Card from './Card.svelte';

	type Props = {
		theme: 'cornsilk' | 'dry-sage';
		title: string;
		children: Snippet;
	};

	let { theme = 'cornsilk', title, children }: Props = $props();
</script>

<Card {theme}>
	<h2 class="p-4 text-center text-lg font-semibold">{title}</h2>
	<div class="space-y-4">
		{@render children()}
	</div>
</Card>
