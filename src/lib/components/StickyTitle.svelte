<script lang="ts">
	import type { Snippet } from 'svelte';

	type Props = {
		children: Snippet;
	};
	let { children }: Props = $props();
</script>

<div class="sticky top-29 w-full bg-white/50 py-4 text-xl backdrop-blur-xl transition-all">
	<div class="container m-auto">
		<h1 class="font-bold text-light-bronze-800">{@render children()}</h1>
	</div>
</div>
