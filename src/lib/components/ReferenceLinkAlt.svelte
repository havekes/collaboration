<script lang="ts">
	type Ref = {
		name: string;
		link: string;
	};

	type Props = {
		refs: Array<Ref>;
		theme: 'dry-sage' | 'cornsilk' | 'light-bronze';
	};

	let { refs, theme }: Props = $props();

	let refCount = $derived(refs.length);
	let linkClasses = $derived.by(() => {
		switch (theme) {
			case 'dry-sage':
				return 'text-dry-sage-800 underline underline-offset-2 hover:text-black';
			case 'cornsilk':
				return 'text-cornsilk-800 underline underline-offset-2 hover:text-black';
			case 'light-bronze':
				return 'text-light-bronze-800 underline underline-offset-2 hover:light-black';
		}
	});
</script>

<p class="text-xs text-gray-700">
	And additional information provided from
	{#each refs as { name, link }, i}
		<a href={'/references#' + link} class={linkClasses}>
			{name}
		</a>{#if refCount > 1 && i + 1 !== refCount},&nbsp;{/if}{#if i + 2 === refCount}and&nbsp;{/if}{/each}.
	{#if refCount === 1}
		This second source is licensed under
	{:else}{/if}
	<a class={linkClasses} href="https://creativecommons.org/licenses/by-nc-nd/4.0/">
		CC BY-NC-ND 4.0
	</a>.
</p>
