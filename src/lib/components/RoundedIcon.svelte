<script lang="ts">
	import { FontAwesomeIcon } from '@fortawesome/svelte-fontawesome';
	let { icon, size = '10', color = 'dry-sage', colorWeight = '200', children } = $props();
</script>

<div class="flex items-center gap-3">
	<div
		style="--color: {color}; --colorWeight: {colorWeight}"
		class="flex h-{size} w-{size} shrink-0 items-center justify-center rounded-full bg-{color}-{colorWeight}"
	>
		<FontAwesomeIcon {icon} class="text-{color}-900" />
	</div>
	<span>{@render children?.()}</span>
</div>
