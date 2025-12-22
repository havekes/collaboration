<script lang="ts">
	import type { Snippet } from 'svelte';

	type Props = {
		theme: 'dry-sage' | 'cornsilk' | 'light-bronze';
		href: string;
		children: Snippet;
	};

	let { theme, href, children }: Props = $props();

	let linkClasses = $derived.by(() => {
		switch (theme) {
			case 'dry-sage':
				return 'text-dry-sage-900 hover:text-dry-sage-700';
			case 'cornsilk':
				return 'text-cornsilk-900 hover:text-cornsilk-700';
			case 'light-bronze':
				return 'text-light-bronze-900 hover:text-light-bronze-700';
		}
	});
</script>

<a {href} class="{linkClasses} transition-all">{@render children()}</a>
