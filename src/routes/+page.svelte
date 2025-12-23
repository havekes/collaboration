<script lang="ts">
	import picture1 from '$lib/assets/images/Picture1.png';
	import HighlightLink from '$lib/components/HighlightLink.svelte';
	import { FontAwesomeIcon } from '@fortawesome/svelte-fontawesome';
	import {
		faHandsHolding,
		faMagnifyingGlass,
		faTriangleExclamation,
		faScaleBalanced,
		faHandshake,
		faArrowsRotate,
		faPersonChalkboard,
		faArrowRight
	} from '@fortawesome/free-solid-svg-icons';
	import RoundedIcon from '$lib/components/RoundedIcon.svelte';
	import Step from '$lib/components/Step.svelte';
	import MainCard from '$lib/components/MainCard.svelte';
	import Card from '$lib/components/Card.svelte';
</script>

<svelte:head>
	<title>Collaboration guide - Comunity-Based Participatory Research</title>
</svelte:head>

<div class="my-16 flex flex-col items-center space-y-24">
	<section class="container rounded-2xl">
		<div class="flex items-center gap-8 text-left">
			<div
				class="flex h-full w-2/3 flex-col items-center justify-center rounded-2xl border border-cornsilk-100 bg-white p-6 shadow-sm shadow-cornsilk-100"
			>
				<img
					src={picture1}
					alt="Key factors to the success of partnerships"
					class="h-auto w-full"
				/>
				<p>Community-based Participatory Research Conceptual Model</p>
				<div class="text-xs text-gray-700">
					<span class="italic">Note.</span> Adapted from Oetzel et al. (2022). The original source
					is licensed under
					<a
						class="underline underline-offset-2"
						href="https://creativecommons.org/licenses/by/4.0/">CC BY 4.0</a
					>
				</div>
			</div>
			<div class="flex-1 space-y-6">
				<h2
					class="text-shadow-corn-silk-200 text-left text-2xl leading-tight font-bold text-cornsilk-900 text-shadow-xs"
				>
					Key factors to the success of partnerships
				</h2>
				<Card theme="cornsilk">
					<h3 class="text-left font-semibold">
						<RoundedIcon icon={faMagnifyingGlass} color="cornsilk" colorWeight="400">
							Want to improve your partnership?
						</RoundedIcon>
					</h3>
					<p class="text-left text-base leading-relaxed text-gray-800">
						See what factors help or hinder collaboration and the success of your partnerships.
					</p>
				</Card>
				<HighlightLink
					href="/facilitators-hindrances"
					text="View facilitators and hindering factors"
					color="cornsilk"
				/>
			</div>
		</div>
	</section>

	<section class="container">
		<div class="flex items-center gap-12 lg:flex-row">
			<div class="w-[calc(100%/3-3.25rem)] space-y-6">
				<h2
					class="text-left text-2xl leading-tight font-bold text-dry-sage-900 text-shadow-dry-sage-200 text-shadow-xs"
				>
					Best practices for effective partnership
				</h2>
				<div class="space-y-6">
					<div class="space-y-6 text-lg">
						<RoundedIcon icon={faHandsHolding}>How to foster it?</RoundedIcon>
						<RoundedIcon icon={faTriangleExclamation}>Why is it important?</RoundedIcon>
					</div>
					<HighlightLink href="/best-practices" text="View best practices" />
				</div>
			</div>
			<Card theme="dry-sage" class="flex-1">
				<div class="grid grid-cols-2 gap-8">
					<!-- Column 1: 1-5 -->
					<div class="flex flex-col gap-4">
						<Step number={1} text="Start Early" />
						<Step number={2} text="Foster Team-Wide Collaboration" />
						<Step number={3} text="Establish Clear Expectations & Common Understanding" />
						<Step number={4} text="Enhance Communication" />
						<Step number={5} text="Demonstrate Impact & Follow Through" />
					</div>
					<!-- Column 2: 6-9 -->
					<div class="flex flex-col gap-4">
						<Step number={6} text="Ensure Adequate Resources" />
						<Step number={7} text="Promote Equitable Decision-Making" />
						<Step number={8} text="Ensure Flexibility" />
						<Step number={9} text="Determine Clear Endpoint" />
					</div>
				</div>
			</Card>
		</div>
	</section>

	<section class="container">
		<div class="flex items-center gap-12 lg:flex-row">
			<div class="w-[calc(100%/3-3.25rem)] space-y-6">
				<h2
					class="text-left text-2xl leading-tight font-bold text-cornsilk-900 text-shadow-cornsilk-200 text-shadow-xs"
				>
					Core Competencies for Equitable Partnership
				</h2>
				<HighlightLink href="/competencies" text="View core competencies" color="cornsilk" />
			</div>
			<Card theme="cornsilk" class="flex-1">
				<RoundedIcon icon={faScaleBalanced} color="cornsilk" colorWeight="300">
					Reflexivity on Identity and Power
				</RoundedIcon>

				<RoundedIcon icon={faHandshake} color="cornsilk" colorWeight="300">
					Understanding Community Context to Work Synergistically
				</RoundedIcon>

				<RoundedIcon icon={faArrowsRotate} color="cornsilk" colorWeight="300">
					Facilitating multidirectional knowledge and skills exchange
				</RoundedIcon>

				<RoundedIcon icon={faPersonChalkboard} color="cornsilk" colorWeight="300">
					Co-Leadership Skills
				</RoundedIcon>

				<RoundedIcon icon={faScaleBalanced} color="cornsilk" colorWeight="300">
					Adaptive Learning Capacity
				</RoundedIcon>
			</Card>
		</div>
	</section>

	<section class="container">
		<div class="space-y-8">
			<div class="grid grid-cols-3 gap-8">
				<MainCard icon={faHandshake} title="Trust" href="/trust-building" link="See trust building">
					Enhancing trust <FontAwesomeIcon icon={faArrowRight} /> to build effective partnership
				</MainCard>

				<MainCard
					icon={faScaleBalanced}
					title="Rolefulness"
					href="/rolefulness"
					link="See rolefulness"
				>
					Understanding roles <FontAwesomeIcon icon={faArrowRight} /> maintain & establish relationship
				</MainCard>

				<MainCard
					icon={faHandsHolding}
					title="Collaborative Alignment"
					href="/collaborative-alignment"
					link="See 4-P foundation"
				>
					Alignment <FontAwesomeIcon icon={faArrowRight} /> collaborative success
				</MainCard>
			</div>
		</div>
	</section>

	<section class="container">
		<div class="flex items-center gap-12 lg:flex-row">
			<div class="w-[calc(100%/3-2.25rem)] space-y-6">
				<h2
					class="text-left text-2xl leading-tight font-bold text-gray-800 text-shadow-cornsilk-200 text-shadow-xs"
				>
					Want to dive deeper?
				</h2>
			</div>
			<div class="w-2/3 flex-1">
				<div class="flex gap-8">
					<Card theme="cornsilk" class="flex-1">
						<HighlightLink
							href="/references"
							text="References"
							color="cornsilk"
							colorWeight="300"
						/>
					</Card>

					<Card theme="cornsilk" class="flex-1">
						<HighlightLink href="/resources" text="Resources" color="cornsilk" colorWeight="300" />
					</Card>
				</div>
			</div>
		</div>
	</section>
</div>
