<script lang="ts">
	import type { Snippet } from 'svelte';

	type Props = {
		children: Snippet;
	};
	let { children }: Props = $props();
</script>

<blockquote
	class="rounded-lg border border-cornsilk-200 bg-cornsilk-50/40 p-4 text-gray-800 italic shadow-cornsilk-100"
>
	{@render children()}
</blockquote>
