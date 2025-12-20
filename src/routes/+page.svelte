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
		faClipboardCheck,
		faArrowRight
	} from '@fortawesome/free-solid-svg-icons';
	import RoundedIcon from '$lib/components/RoundedIcon.svelte';
	import Step from '$lib/components/Step.svelte';
	import MainCard from '$lib/components/MainCard.svelte';
</script>

<div class="my-12 flex flex-col items-center space-y-16">
	<section class="container rounded-2xl bg-cornsilk-100 p-8">
		<div class="flex items-center gap-8 text-left">
			<div class="flex h-full w-2/3 items-center justify-center rounded-2xl p-6">
				<img
					src={picture1}
					alt="Key factors to the success of partnerships"
					class="h-auto w-full rounded-xl"
				/>
			</div>
			<div class="flex-1 space-y-6">
				<h2
					class="text-shadow-corn-silk-200 text-left text-2xl leading-tight font-bold text-gray-800 text-shadow-xs"
				>
					Key factors to the success of partnerships
				</h2>
				<div
					class="space-y-2 rounded-2xl border border-cornsilk-400 bg-linear-to-br from-cornsilk-200 to-cornsilk-300 p-6 shadow-md shadow-cornsilk-200"
				>
					<h3 class="text-left font-semibold">
						<RoundedIcon icon={faMagnifyingGlass} color="cornsilk" colorWeight="400">
							Want to improve your partnership?
						</RoundedIcon>
					</h3>
					<p class="text-left text-base leading-relaxed text-gray-800">
						See what factors help or hinder collaboration and the success of your partnerships.
					</p>
				</div>
				<HighlightLink href="#" text="View facilitators and hindering factors" color="cornsilk" />
			</div>
		</div>
	</section>

	<section class="container px-8">
		<div class="flex items-center gap-12 lg:flex-row">
			<div class="w-[calc(100%/3-3.25rem)] space-y-6">
				<h2
					class="text-left text-2xl leading-tight font-bold text-gray-800 text-shadow-dry-sage-200 text-shadow-xs"
				>
					Best practices for effective partnership
				</h2>
				<div class="space-y-6 text-lg">
					<RoundedIcon icon={faHandsHolding}>How to foster it?</RoundedIcon>
					<RoundedIcon icon={faTriangleExclamation}>Why is it important?</RoundedIcon>
					<HighlightLink href="#" text="View best practices" />
				</div>
			</div>
			<div class="w-2/3 flex-1">
				<div
					class="rounded-2xl border border-dry-sage-200 bg-linear-to-br from-dry-sage-50 to-dry-sage-100 p-6 shadow-md shadow-dry-sage-100"
				>
					<div class="grid grid-cols-2 gap-8">
						<!-- Column 1: 1-5 -->
						<div class="flex flex-col gap-4">
							<Step number={1} text="Start Early" />
							<Step number={2} text="Foster Team-Wide Collaboration" />
							<Step number={3} text="Establish expectations & common understanding" />
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
				</div>
			</div>
		</div>
	</section>

	<section class="container rounded-2xl bg-cornsilk-100 p-8">
		<div class="flex items-center gap-12 lg:flex-row">
			<div class="w-[calc(100%/3-3.25rem)] space-y-6">
				<h2
					class="text-left text-2xl leading-tight font-bold text-gray-800 text-shadow-cornsilk-200 text-shadow-xs"
				>
					Core Competencies for Equitable Partnership
				</h2>
			</div>
			<div class="w-2/3 flex-1">
				<div
					class="space-y-2 rounded-2xl border border-cornsilk-400 bg-linear-to-br from-cornsilk-200 to-cornsilk-300 p-6 shadow-md shadow-cornsilk-200"
				>
					<div class="space-y-4">
						<RoundedIcon icon={faScaleBalanced} color="cornsilk" colorWeight="400">
							Capacity to interpret and respond to individual and relational identity, connection,
							uniqueness and inequities
						</RoundedIcon>

						<RoundedIcon icon={faHandshake} color="cornsilk" colorWeight="400">
							Ability of communities and partners to work in the most suitable, inclusive and
							synergistic way
						</RoundedIcon>

						<RoundedIcon icon={faArrowsRotate} color="cornsilk" colorWeight="400">
							Aptitude for generating safe and inclusive spaces for multidirectional knowledge and
							skills exchange
						</RoundedIcon>

						<RoundedIcon icon={faPersonChalkboard} color="cornsilk" colorWeight="400">
							Expertise in democratic leadership and/or facilitation to balance competing
							prioritiesReferences and ensure shared decision-making
						</RoundedIcon>

						<RoundedIcon icon={faScaleBalanced} color="cornsilk" colorWeight="400">
							Capacity to interpret and respond to individual and relational identity, connection,
							uniqueness and inequities
						</RoundedIcon>
					</div>
				</div>
			</div>
		</div>
	</section>

	<section class="container">
		<div class="space-y-8">
			<div class="grid grid-cols-1 gap-6 lg:grid-cols-3 lg:gap-8">
				<MainCard icon={faHandshake} title="Trust" link="See trust building">
					Enhancing trust <FontAwesomeIcon icon={faArrowRight} /> to build effective partnership
				</MainCard>

				<MainCard icon={faScaleBalanced} title="Rolefulness" link="See rolefulness">
					Understanding roles <FontAwesomeIcon icon={faArrowRight} /> maintain & establish relationship
				</MainCard>

				<MainCard icon={faHandsHolding} title="Collaborative Alignment" link="See 4-P foundation">
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
					<div
						class="flex-1 space-y-2 rounded-2xl border border-cornsilk-400 bg-linear-to-br from-cornsilk-200 to-cornsilk-300 p-6 shadow-md shadow-cornsilk-200"
					>
						<HighlightLink href="" text="References" color="cornsilk" colorWeight="400" />
					</div>

					<div
						class="flex-1 space-y-2 rounded-2xl border border-cornsilk-400 bg-linear-to-br from-cornsilk-200 to-cornsilk-300 p-6 shadow-md shadow-cornsilk-200"
					>
						<HighlightLink href="" text="Resources" color="cornsilk" colorWeight="400" />
					</div>
				</div>
			</div>
		</div>
	</section>
</div>
