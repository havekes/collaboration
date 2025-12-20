<script>
	import { FontAwesomeIcon } from '@fortawesome/svelte-fontawesome';
	import HighlightLink from './HighlightLink.svelte';

	let { icon, title, link, children } = $props();
</script>

<div
	class="flex items-center gap-8 rounded-2xl border border-dry-sage-200 bg-linear-to-br from-dry-sage-50 to-dry-sage-100 p-6 shadow-md shadow-dry-sage-100"
>
	<div class="flex h-12 w-12 shrink-0 items-center justify-center rounded-full bg-dry-sage-200">
		<FontAwesomeIcon {icon} class="text-xl text-dry-sage-800" />
	</div>
	<div class="flex h-full w-full flex-col space-y-4">
		<h3 class=" text-lg font-semibold text-gray-800">{title}</h3>
		<div class="flex flex-1 items-center">
			<p class="text-base leading-relaxed text-gray-700">
				{@render children?.()}
			</p>
		</div>
		<HighlightLink href="#" text={link} />
	</div>
</div>
