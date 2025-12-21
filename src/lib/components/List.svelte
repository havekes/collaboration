<script lang="ts">
	import type { Snippet } from 'svelte';

	type Props = {
		title: string;
		children: Snippet;
	};

	let { title, children }: Props = $props();
</script>

<div class="space-y-2">
	<h3 class="font-semibold">{title}</h3>
	<ul class="space-y-1">
		{@render children()}
	</ul>
</div>
