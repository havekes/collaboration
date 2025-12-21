<script lang="ts">
	import { faArrowRight } from '@fortawesome/free-solid-svg-icons';
	import { FontAwesomeIcon } from '@fortawesome/svelte-fontawesome';

	let { href, text, color = 'dry-sage', colorWeight = '200' } = $props();
</script>

<div class="group flex items-center justify-between gap-2 text-{color}-900">
	<a {href} class="font-semibold transition-colors duration-200 group-hover:text-{color}-700">
		{text}
	</a>
	<a
		{href}
		class="rounded-full bg-{color}-{colorWeight} p-2 transition-all duration-200 group-hover:translate-x-2"
		aria-label="View details"
	>
		<div class="flex h-6 w-6 items-center justify-center">
			<FontAwesomeIcon icon={faArrowRight} />
		</div>
	</a>
</div>
