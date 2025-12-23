<script lang="ts">
	import type { Snippet } from 'svelte';

	type Props = {
		link: string;
		children: Snippet;
	};

	let { link, children }: Props = $props();
</script>

<p class="ml-12 -indent-12" id={link}>
	{@render children()}
	<a
		href={link}
		class="text-light-bronze-700 underline underline-offset-2 hover:text-light-bronze-900">{link}</a
	>
</p>
