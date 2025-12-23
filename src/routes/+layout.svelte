<script lang="ts">
	import './layout.css';
	import favicon from '$lib/assets/favicon.svg';
	import MenuItem from '$lib/components/MenuItem.svelte';
	import type { Snippet } from 'svelte';
	import { page } from '$app/state';

	type Props = {
		children: Snippet;
	};
	type MenuItemData = {
		name: string;
		href: string;
	};

	let { children }: Props = $props();

	let scrollY = $state(0);

	let scrollClasses = $derived(
		scrollY > 0 ? 'bg-cornsilk-800/80 backdrop-blur-xl' : 'bg-cornsilk-800'
	);

	let menuItems: Array<MenuItemData> = [
		{ name: 'Facilitators & Hindrances', href: '/facilitators-hindrances' },
		{ name: 'Best Practices', href: '/best-practices' },
		{ name: 'Competencies', href: '/competencies' },
		{ name: 'Trust', href: '/trust-building' },
		{ name: 'Rolefulness', href: '/rolefulness' },
		{ name: 'Collaborative alignment', href: '/collaborative-alignment' }
	];
</script>

<svelte:head><link rel="icon" href={favicon} /></svelte:head>

<svelte:window bind:scrollY />

<div>
	<header class="sticky top-0 z-50 w-full py-8 {scrollClasses} transition-all">
		<div class="container m-auto flex items-center">
			<a
				class="flex flex-col rounded-full text-cornsilk-100 transition-all hover:-mx-8 hover:-my-4 hover:bg-white/10 hover:px-8 hover:py-4 hover:text-cornsilk-50"
				href="/"
			>
				<span class="text-2xl font-bold">Collaboration guide</span>
				<span class="text-sm">Comunity-Based Participatory Research</span>
			</a>
			<menu class="flex flex-1 justify-end gap-2">
				{#each menuItems as item}
					<MenuItem href={item.href} active={page.url.pathname === item.href}>{item.name}</MenuItem>
				{/each}
			</menu>
		</div>
	</header>
	{@render children()}
</div>
