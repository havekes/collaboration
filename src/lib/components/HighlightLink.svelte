<script lang="ts">
	import { faArrowRight } from '@fortawesome/free-solid-svg-icons';
	import { FontAwesomeIcon } from '@fortawesome/svelte-fontawesome';

	export let href: string = '#';
	export let text: string = '';
</script>

<div class="group flex items-center justify-between gap-2">
	<a {href} class="font-semibold transition-colors duration-200 hover:text-dry-sage-600">
		{text}
	</a>
	<a
		{href}
		class="rounded-full bg-dry-sage-200 p-2 text-dry-sage-800 transition-all duration-200 group-hover:translate-x-1"
		aria-label="View details"
	>
		<FontAwesomeIcon icon={faArrowRight} class="text-dry-sage-800" />
	</a>
</div>
