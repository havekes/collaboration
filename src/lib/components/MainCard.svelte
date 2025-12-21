<script>
	import { FontAwesomeIcon } from '@fortawesome/svelte-fontawesome';
	import HighlightLink from './HighlightLink.svelte';
	import Card from './Card.svelte';

	let { icon, title, link, href = '#', children } = $props();
</script>

<Card theme="dry-sage" class="flex items-center gap-8">
	<div class="flex h-12 w-12 shrink-0 items-center justify-center rounded-full bg-dry-sage-300">
		<FontAwesomeIcon {icon} class="text-xl text-dry-sage-800" />
	</div>
	<div class="flex h-full w-full flex-col space-y-4">
		<h3 class=" text-lg font-semibold text-gray-800">{title}</h3>
		<div class="flex flex-1 items-center">
			<p class="text-base leading-relaxed text-gray-700">
				{@render children()}
			</p>
		</div>
		<HighlightLink {href} text={link} colorWeight="300" />
	</div>
</Card>
