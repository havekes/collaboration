<script lang="ts">
	import { slide, fade, scale } from 'svelte/transition';

	export let theme: 'cornsilk' | 'dry-sage';
	export let title: string;
	export let open: boolean;
	export let onToggle: () => void;
	type AccordionItemType = string | Record<string, string[]>;
	export let leftContent: any[] = [];
	export let rightContent: any[] = [];

	$: containerClasses =
		theme === 'cornsilk'
			? 'scale-95 border border-cornsilk-400 bg-gradient-to-br from-cornsilk-200 to-cornsilk-300 shadow-sm shadow-cornsilk-200'
			: 'scale-95 border border-dry-sage-200 bg-gradient-to-br from-dry-sage-50 to-dry-sage-100 shadow-sm shadow-dry-sage-100';
</script>

<div
	class="overflow-hidden rounded-2xl {containerClasses} transition-all duration-300 hover:scale-100 hover:shadow-md"
	class:scale-100={open}
>
	<button
		class="flex w-full cursor-pointer items-center justify-between px-8 py-6 text-left"
		on:click={onToggle}
	>
		<h2 class="text-xl font-bold text-dry-sage-800">{title}</h2>
		<svg
			class="h-8 w-8 transition-transform duration-300 {open ? 'rotate-180' : ''}"
			fill="none"
			stroke="currentColor"
			viewBox="0 0 24 24"
		>
			<path
				stroke-linecap="round"
				stroke-linejoin="round"
				stroke-width="2"
				d="M19 9l-7 7-7-7"
				class="stroke-dry-sage-700"
			></path>
		</svg>
	</button>
	{#if open}
		<div class="px-8 lg:pb-10" transition:slide|local={{ duration: 400 }}>
			<div class="grid grid-cols-2 gap-8">
				<div class="space-y-4">
					<h3 class="font-semibold text-dry-sage-800">How to foster it?</h3>
					<ul class="space-y-3 text-gray-700">
						{#each leftContent as item, index}
							{#if typeof item === 'object'}
								{@const subItems = Object.values(item)[0] as Array<string>}
								<li
									class="flex items-start"
									transition:fade|local={{ delay: 150 + index * 75, duration: 300 }}
								>
									<svg
										class="mt-0.5 h-6 w-6 shrink-0 text-dry-sage-500"
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
										<ul class="mt-2 ml-3 space-y-2">
											{#each subItems as subItem}
												<li class="flex items-start">
													<svg
														class="h-5 w-5 shrink-0 text-dry-sage-500"
														fill="currentColor"
														viewBox="0 0 20 20"
													>
														<path
															fill-rule="evenodd"
															d="M13.707 9.707a1 1 0 00-1.414-1.414L9 12.586 7.707 11.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
															clip-rule="evenodd"
														></path>
													</svg>
													<span class="ml-2 text-sm">{subItem}</span>
												</li>
											{/each}
										</ul>
									</div>
								</li>
							{:else}
								<li
									class="flex items-start"
									transition:fade|local={{ delay: 150 + index * 75, duration: 300 }}
								>
									<svg
										class="mt-0.5 h-6 w-6 shrink-0 text-dry-sage-500"
										fill="currentColor"
										viewBox="0 0 20 20"
									>
										<path
											fill-rule="evenodd"
											d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
											clip-rule="evenodd"
										></path>
									</svg>
									<span class="ml-3 text-gray-700">{item}</span>
								</li>
							{/if}
						{/each}
					</ul>
				</div>
				<div class="space-y-4">
					<h3 class="font-semibold text-dry-sage-800">Why do it?</h3>
					<ul class="space-y-3">
						{#each rightContent as item, index}
							<li
								class="flex items-start"
								transition:fade|local={{ delay: 200 + index * 75, duration: 300 }}
							>
								<svg
									class="mt-0.5 h-6 w-6 shrink-0 text-dry-sage-500"
									fill="currentColor"
									viewBox="0 0 20 20"
								>
									<path
										fill-rule="evenodd"
										d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
										clip-rule="evenodd"
									></path>
								</svg>
								<span class="ml-3 text-gray-700">{item}</span>
							</li>
						{/each}
					</ul>
				</div>
			</div>
		</div>
	{/if}
</div>
