<script lang="ts">
	export let number: number;
	export let text: string;
</script>

<div class="flex items-center gap-4">
	<div
		class="flex h-10 w-10 shrink-0 items-center justify-center rounded-full bg-dry-sage-200 text-lg font-bold text-dry-sage-800"
	>
		{number}
	</div>
	<span class="flex-1 text-base font-normal text-gray-700">{text}</span>
</div>
