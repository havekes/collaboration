<script>
	import Link from '$lib/components/Link.svelte';
	import ListItem from '$lib/components/ListItem.svelte';
	import StickyTitle from '$lib/components/StickyTitle.svelte';
</script>

<svelte:head>
	<title>Additional resources</title>
</svelte:head>

<div class="my-8 flex flex-col items-center space-y-4">
	<section class="container">
		<h1 class="text-3xl font-bold text-cornsilk-800">Additional resources</h1>
	</section>

	<StickyTitle>Fostering Equitable Collaboration</StickyTitle>
	<div class="container w-full">
		<ListItem theme="cornsilk">
			<Link
				theme="cornsilk"
				href="https://nonprofitquarterly.org/collaborating-equity-justice-moving-beyond-collective-impact/"
			>
				Collaborating for Equity and Justice: Moving Beyond Collective Impact
			</Link>
		</ListItem>
	</div>

	<StickyTitle>Enhancing collaboration: Strategies and Skills</StickyTitle>
	<div class="container w-full space-y-4">
		<ListItem theme="cornsilk">
			<Link theme="cornsilk" href="https://positivepsychology.com/collaboration/">
				Enhancing Collaboration In The Workplace: 5 Strategies
			</Link>
		</ListItem>
		<ListItem theme="cornsilk">
			<iframe
				width="560"
				height="315"
				src="https://www.youtube.com/embed/vjSTNv4gyMM?si=oUayJw2ATFAydSwR"
				title="YouTube video player"
				frameborder="0"
				allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
				referrerpolicy="strict-origin-when-cross-origin"
				allowfullscreen
			></iframe>
		</ListItem>
	</div>

	<StickyTitle>Steps for effective communication</StickyTitle>
	<div class="container w-full">
		<ListItem theme="cornsilk">
			<Link
				theme="cornsilk"
				href="https://professional.brown.edu/news/2024-06-14/effective-communication"
			>
				Five steps for effective communication
			</Link>
		</ListItem>
	</div>

	<StickyTitle>Fostering partnership in community engagement</StickyTitle>
	<div class="container w-full space-y-3">
		<ListItem theme="cornsilk">
			<Link
				theme="cornsilk"
				href="https://www.urban.org/research/publication/fostering-partnerships-community-engagement"
			>
				Toolkit: Fostering Partnerships for Community Engagement
			</Link>
		</ListItem>
		<ListItem theme="cornsilk">
			<Link
				theme="cornsilk"
				href="https://nmhec.org/wp-content/uploads/CBPR-Toolkit_FINAL_v3_ada.pdf"
			>
				A step-by-step guide to community based participatory research
			</Link>
		</ListItem>
		<ListItem theme="cornsilk">
			<Link
				theme="cornsilk"
				href="https://accelerate.ucsf.edu/sites/default/files/CE/manual_for_researchers_agencies.pdf"
			>
				Community-Engaged Research with Community-Based Organizations: A Resource Manual for
				Researchers
			</Link>
		</ListItem>
	</div>
</div>
