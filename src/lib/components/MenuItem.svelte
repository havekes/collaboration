<script lang="ts">
	import type { Snippet } from 'svelte';

	type Props = {
		active?: boolean;
		href?: string;
		children: Snippet;
	};
	let { active = false, href = '#', children }: Props = $props();

	let activeClasses = $derived(
		active
			? 'mx-0 my-0 bg-cornsilk-100 px-4 py-3 text-cornsilk-900 backdrop-blur-xl'
			: 'mx-4 my-3 hover:mx-0 hover:my-0 hover:bg-cornsilk-100 hover:px-4 hover:py-3 hover:text-cornsilk-900 hover:backdrop-blur-xl'
	);
</script>

<menuitem>
	<a
		{href}
		class="hover rounded-full font-semibold {activeClasses} text-cornsilk-100 transition-all"
	>
		{@render children()}
	</a>
</menuitem>
