<script lang="ts">
	let { children } = $props();
</script>

<li class="flex items-start">
	<svg class="h-5 w-5 shrink-0 text-dry-sage-500" fill="currentColor" viewBox="0 0 20 20">
		<path
			fill-rule="evenodd"
			d="M13.707 9.707a1 1 0 00-1.414-1.414L9 12.586 7.707 11.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
			clip-rule="evenodd"
		></path>
	</svg>
	<span class="ml-2 text-gray-700">{@render children()}</span>
</li>
