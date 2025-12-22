<script lang="ts">
	import { fade } from 'svelte/transition';
	import List from './List.svelte';
	import ListItem from './ListItem.svelte';

	type Content = Array<string | Record<string, Array<string>>>;
	type Props = {
		theme: 'cornsilk' | 'dry-sage';
		content: Content;
	};

	let { theme, content }: Props = $props();
	let markerClasses = $derived(theme === 'cornsilk' ? 'text-cornsilk-500' : 'text-dry-sage-500');
</script>

<ul class="space-y-3 text-gray-700">
	{#each content as item, index}
		{#if typeof item === 'object'}
			{@const subItems = Object.values(item)[0] as Array<string>}
			<li
				class="flex items-start"
				transition:fade|local={{ delay: 150 + index * 75, duration: 300 }}
			>
				<svg
					class="mt-0.5 h-6 w-6 shrink-0 {markerClasses}"
					fill="currentColor"
					viewBox="0 0 20 20"
				>
					<path
						fill-rule="evenodd"
						d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
						clip-rule="evenodd"
					></path>
				</svg>
				<div>
					<p class="ml-3">{Object.keys(item)[0]}:</p>
					<List>
						<div class="mt-2 ml-2 space-y-2 text-sm">
							{#each subItems as subItem}
								<ListItem {theme}>
									{subItem}
								</ListItem>
							{/each}
						</div>
					</List>
				</div>
			</li>
		{:else}
			<li
				class="flex items-start"
				transition:fade|local={{ delay: 150 + index * 75, duration: 300 }}
			>
				<svg
					class="mt-0.5 h-6 w-6 shrink-0 {markerClasses}"
					fill="currentColor"
					viewBox="0 0 20 20"
				>
					<path
						fill-rule="evenodd"
						d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
						clip-rule="evenodd"
					></path>
				</svg>
				<span class="ml-3 text-gray-800">{item}</span>
			</li>
		{/if}
	{/each}
</ul>
