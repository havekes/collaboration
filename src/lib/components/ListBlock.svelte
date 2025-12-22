<script lang="ts">
	import type { Snippet } from 'svelte';
	import Card from './Card.svelte';
	import CardTitle from './CardTitle.svelte';

	type Props = {
		theme: 'cornsilk' | 'dry-sage';
		title: string;
		children: Snippet;
	};

	let { theme = 'cornsilk', title, children }: Props = $props();
</script>

<Card {theme}>
	<CardTitle {theme}>{title}</CardTitle>
	<div class="space-y-4">
		{@render children()}
	</div>
</Card>
