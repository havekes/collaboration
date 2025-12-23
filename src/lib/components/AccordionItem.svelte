<script lang="ts">
	import slugify from 'slugify';
	import { slide } from 'svelte/transition';
	import AccordionContent from './AccordionContent.svelte';
	import { page } from '$app/state';
	import ReferenceLink from './ReferenceLink.svelte';
	import ReferenceLinkAlt from './ReferenceLinkAlt.svelte';

	type Content = Array<string | Record<string, Array<string>>>;
	type Ref = {
		name: string;
		link: string;
		alt?: boolean;
	};
	type Props = {
		theme: 'cornsilk' | 'dry-sage';
		title: string;
		id?: string;
		open: boolean;
		onToggle: () => void;
		leftTitle?: string;
		leftContent: Content;
		rightTitle: string;
		rightContent: Content;
		middleTitle?: string;
		middleContent?: Content;
		refs: Array<Ref>;
		refsAlt?: Array<Ref>;
	};

	let {
		theme,
		title,
		id,
		open,
		onToggle,
		leftTitle,
		leftContent,
		rightTitle,
		rightContent,
		middleTitle,
		middleContent,
		refs,
		refsAlt
	}: Props = $props();

	let containerClasses = $derived(
		theme === 'cornsilk'
			? 'border-cornsilk-200 bg-linear-to-br from-cornsilk-100 to-cornsilk-200 shadow-cornsilk-100'
			: 'border-dry-sage-200 bg-linear-to-br from-dry-sage-100 to-dry-sage-200 shadow-dry-sage-100'
	);
	let titleClasses = $derived(theme === 'cornsilk' ? 'text-cornsilk-900' : 'text-dry-sage-900');
	let subTitleClasses = $derived(theme === 'cornsilk' ? 'text-cornsilk-800' : 'text-dry-sage-800');
	let markerClasses = $derived(theme === 'cornsilk' ? 'text-cornsilk-500' : 'text-dry-sage-500');
	let gridClasses = $derived(middleContent ? 'grid-cols-3' : 'grid-cols-2');

	let computedId = $derived(id ?? slugify(title));
	let currentAnchor = $derived(page.url.hash);
	let computedOpen = $derived(open ? true : currentAnchor.slice(1) == computedId);
</script>

<div
	class="scale-95 overflow-hidden rounded-2xl border shadow-sm transition-all duration-300 hover:scale-100 hover:shadow-md {containerClasses}"
	class:scale-100={open}
>
	<div id={computedId} class="relative -top-68"></div>
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

	{#if computedOpen}
		<div class="px-8 pb-8" transition:slide|local={{ duration: 400 }}>
			<div class="grid {gridClasses} grid-cols-2 gap-8">
				<div class="space-y-4">
					<h3 class="font-semibold {subTitleClasses}">{leftTitle}</h3>
					<AccordionContent {theme} content={leftContent} />
				</div>
				{#if middleContent}
					<div class="space-y-4">
						<h3 class="font-semibold {subTitleClasses}">{middleTitle}</h3>
						<AccordionContent {theme} content={middleContent} />
					</div>
				{/if}
				<div class="space-y-4">
					<h3 class="font-semibold {subTitleClasses}">{rightTitle}</h3>
					<AccordionContent {theme} content={rightContent} />
				</div>
			</div>
			<div class="mt-4">
				<ReferenceLink {theme} {refs} />
				{#if refsAlt}
					<ReferenceLinkAlt {theme} refs={refsAlt} />
				{/if}
			</div>
		</div>
	{/if}
</div>
