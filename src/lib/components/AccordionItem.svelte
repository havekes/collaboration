<script lang="ts">
	import { slide, fade } from 'svelte/transition';
	import List from './List.svelte';
	import ListItem from './ListItem.svelte';

	type Content = Array<string | Record<string, Array<string>>>;
	type Props = {
		theme: 'cornsilk' | 'dry-sage';
		title: string;
		open: boolean;
		onToggle: () => void;
		leftContent?: Content;
		rightContent?: Content;
	};

	let { theme, title, open, onToggle, leftContent, rightContent }: Props = $props();

	let containerClasses = $derived(
		theme === 'cornsilk'
			? 'border-cornsilk-200 bg-linear-to-br from-cornsilk-100 to-cornsilk-200 shadow-cornsilk-100'
			: 'border-dry-sage-200 bg-linear-to-br from-dry-sage-100 to-dry-sage-200 shadow-dry-sage-100'
	);
	let titleClasses = $derived(theme === 'cornsilk' ? 'text-cornsilk-900' : 'text-dry-sage-900');
	let subTitleClasses = $derived(theme === 'cornsilk' ? 'text-cornsilk-800' : 'text-dry-sage-800');
	let markerClasses = $derived(theme === 'cornsilk' ? 'text-cornsilk-500' : 'text-dry-sage-500');
</script>

<div
	class="scale-95 overflow-hidden rounded-2xl border shadow-sm transition-all duration-300 hover:scale-100 hover:shadow-md {containerClasses}"
	class:scale-100={open}
>
	<button
		class="flex w-full cursor-pointer items-center justify-between px-8 py-6 text-left"
		onclick={onToggle}
	>
		<h2 class="text-xl font-bold {titleClasses}">{title}</h2>
		<svg
			class="h-8 w-8 transition-transform duration-300 {open ? 'rotate-180' : ''} {titleClasses}"
			fill="none"
			stroke="currentColor"
			viewBox="0 0 24 24"
		>
			<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"
			></path>
		</svg>
	</button>
	{#if open}
		<div class="px-8 pb-8" transition:slide|local={{ duration: 400 }}>
			<div class="grid grid-cols-2 gap-8">
				<div class="space-y-4">
					<h3 class="font-semibold {subTitleClasses}">How to foster it?</h3>
					<ul class="space-y-3 text-gray-700">
						{#each leftContent as item, index}
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
											<div class="mt-2 ml-2 text-sm">
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
				</div>
				<div class="space-y-4">
					<h3 class="font-semibold {subTitleClasses}">Why do it?</h3>
					<ul class="space-y-3">
						{#each rightContent as item, index}
							<li
								class="flex items-start"
								transition:fade|local={{ delay: 200 + index * 75, duration: 300 }}
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
						{/each}
					</ul>
				</div>
			</div>
		</div>
	{/if}
</div>
