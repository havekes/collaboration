<script lang="ts">
	import type { Snippet } from 'svelte';

	type Props = {
		children: Snippet;
	};
	let { children }: Props = $props();

	let scrollY = $state(0);

	let scrollClasses = $derived(
		scrollY > 0 ? 'bg-corn-700/80 backdrop-blur-xl text-xl py-2' : 'bg-cornsilk-700 py-4 text-3xl'
	);
</script>

<svelte:window bind:scrollY />

<div class="fixed top-24 w-full {scrollClasses} transition-all">
	<div class="container m-auto">
		<h1 class="font-bold text-cornsilk-100 text-shadow-xs">{@render children()}</h1>
	</div>
</div>
