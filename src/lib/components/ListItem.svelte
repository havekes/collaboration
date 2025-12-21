<script lang="ts">
	import type { Snippet } from 'svelte';

	type Props = {
		theme?: 'dry-sage' | 'cornsilk' | 'light-bronze';
		children: Snippet;
	};

	let { theme = 'dry-sage', children }: Props = $props();

	let iconClasses = $derived.by(() => {
		switch (theme) {
			case 'dry-sage':
				return 'text-dry-sage-500';
			case 'cornsilk':
				return 'text-cornsilk-500';
			case 'light-bronze':
				return 'text-light-bronze-500';
		}
	});
</script>

<li class="flex items-start">
	<svg class="h-5 w-5 shrink-0 {iconClasses}" fill="currentColor" viewBox="0 0 20 20">
		<path
			fill-rule="evenodd"
			d="M13.707 9.707a1 1 0 00-1.414-1.414L9 12.586 7.707 11.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
			clip-rule="evenodd"
		></path>
	</svg>
	<span class="ml-2 text-gray-800">{@render children()}</span>
</li>
