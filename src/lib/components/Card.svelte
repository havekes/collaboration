<script lang="ts">
	import type { Snippet } from 'svelte';

	type Props = {
		theme: 'dry-sage' | 'cornsilk' | 'light-bronze';
		class?: string;
		children: Snippet;
	};

	let { theme, class: classes = undefined, children }: Props = $props();

	let themeClasses = $derived.by(() => {
		switch (theme) {
			case 'dry-sage':
				return 'border-dry-sage-200 bg-linear-to-br from-dry-sage-100 to-dry-sage-200 shadow-dry-sage-100';
			case 'cornsilk':
				return 'border-cornsilk-200 bg-linear-to-br from-cornsilk-100 to-cornsilk-200 shadow-cornsilk-100';
			case 'light-bronze':
				return 'border-light-bronze-200 bg-linear-to-br from-light-bronze-100 to-light-bronze-200 shadow-light-bronze-100';
		}
	});
</script>

<div
	class="space-y-4 rounded-2xl border p-6 shadow-sm {themeClasses} {classes ?? ''} flex flex-col"
>
	{@render children()}
</div>
