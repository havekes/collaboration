<script lang="ts">
	import type { Snippet } from 'svelte';

	type Props = {
		theme: 'dry-sage' | 'cornsilk' | 'light-bronze';
		children: Snippet;
	};

	let { theme, children }: Props = $props();

	let themeClasses = $derived.by(() => {
		switch (theme) {
			case 'dry-sage':
				return 'border-dry-sage-200  from-dry-sage-50 to-dry-sage-100 text-dry-sage-900';
			case 'cornsilk':
				return 'border-cornsilk-200 from-cornsilk-50 to-cornsilk-100 text-cornsilk-900';
			case 'light-bronze':
				return 'border-light-bronze-200 from-light-bronze-50 to-light-bronze-100 text-light-bronze-900';
		}
	});
</script>

<div class="rounded-lg border bg-linear-to-br p-4 {themeClasses}">
	<h2 class="text-center text-lg font-bold">{@render children()}</h2>
</div>
