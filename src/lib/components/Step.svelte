<script lang="ts">
	type Props = {
		number: number;
		text: string;
	};

	let { number, text }: Props = $props();
</script>

<div class="flex items-center gap-4">
	<div
		class="flex h-10 w-10 shrink-0 items-center justify-center rounded-full bg-dry-sage-300 text-lg font-bold text-dry-sage-900"
	>
		{number}
	</div>
	<span class="flex-1 text-base font-normal text-gray-800">{text}</span>
</div>
