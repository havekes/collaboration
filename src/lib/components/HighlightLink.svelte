<script lang="ts">
	import { faArrowRight } from '@fortawesome/free-solid-svg-icons';
	import { FontAwesomeIcon } from '@fortawesome/svelte-fontawesome';

	let { href, text, color = 'dry-sage', colorWeight = '200' } = $props();
</script>

<div class="group flex items-center justify-between gap-2">
	<a {href} class="font-semibold transition-colors duration-200 group-hover:text-{color}-800">
		{text}
	</a>
	<a
		{href}
		class="rounded-full bg-{color}-{colorWeight} p-2 text-{color}-800 transition-all duration-200 group-hover:translate-x-1"
		aria-label="View details"
	>
		<FontAwesomeIcon icon={faArrowRight} class="text-{color}-800" />
	</a>
</div>
