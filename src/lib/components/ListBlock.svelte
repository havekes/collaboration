<script lang="ts">
	import type { Snippet } from 'svelte';

	type Props = {
		theme: 'cornsilk' | 'dry-sage';
		title: string;
		children: Snippet;
	};

	let { theme = 'cornsilk', title, children }: Props = $props();

	let containerClasses = $derived(
		'space-y-4 rounded-2xl border p-6 ' +
			(theme == 'cornsilk'
				? 'border-cornsilk-400 bg-linear-to-br from-cornsilk-200 to-cornsilk-300 shadow-sm shadow-cornsilk-200'
				: 'border-dry-sage-200 bg-linear-to-br from-dry-sage-50 to-dry-sage-100 shadow-sm shadow-dry-sage-100')
	);
</script>

<div class={containerClasses}>
	<h2 class="p-4 text-center text-lg font-semibold">{title}</h2>
	<div class="space-y-4">
		{@render children()}
	</div>
</div>
