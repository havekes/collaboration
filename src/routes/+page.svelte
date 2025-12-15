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
		faClipboardCheck
	} from '@fortawesome/free-solid-svg-icons';
	import Step from '$lib/components/Step.svelte';
</script>

<section class="container m-auto py-8">
	<div class="flex items-center gap-8 text-left">
		<div class="flex h-full w-2/3 items-center justify-center p-6">
			<img
				src={picture1}
				alt="Key factors to the success of partnerships"
				class="h-auto w-full rounded-xl"
			/>
		</div>
		<div class="flex-1 space-y-4">
			<h2
				class="text-left text-2xl leading-tight font-bold text-gray-800 text-shadow-dry-sage-200 text-shadow-xs"
			>
				Key factors to the success of partnerships
			</h2>
			<div
				class="space-y-2 rounded-2xl border border-dry-sage-200 bg-gradient-to-br from-dry-sage-50 to-dry-sage-100 p-6 shadow-md shadow-dry-sage-100"
			>
				<h3 class="text-left font-semibold">
					<div class="flex items-center gap-3">
						<div
							class="flex h-10 w-10 shrink-0 items-center justify-center rounded-full bg-dry-sage-200"
						>
							<FontAwesomeIcon icon={faMagnifyingGlass} class="text-dry-sage-800" />
						</div>
						<span>Want to improve your partnership?</span>
					</div>
				</h3>
				<p class="text-left text-base leading-relaxed text-gray-800">
					See what factors help or hinder collaboration and the success of your partnerships.
				</p>
			</div>
			<HighlightLink href="#" text="View facilitators and hindering factors" />
		</div>
	</div>
</section>

<section class="container m-auto mt-12">
	<div class="flex items-center gap-8 lg:flex-row">
		<!-- Left 1/3 card -->
		<div class="w-full space-y-6 lg:w-1/3">
			<h2
				class="text-left text-2xl leading-tight font-bold text-gray-800 text-shadow-dry-sage-200 text-shadow-xs"
			>
				Best practices for effective partnership
			</h2>
			<div class="space-y-2 text-lg">
				<div class="flex items-center gap-3 p-2">
					<div
						class="flex h-10 w-10 shrink-0 items-center justify-center rounded-full bg-dry-sage-200"
					>
						<FontAwesomeIcon icon={faHandsHolding} class="text-dry-sage-800" />
					</div>
					<span class="text-gray-700">How to foster it?</span>
				</div>
				<div class="flex items-center gap-3 p-2">
					<div
						class="flex h-10 w-10 shrink-0 items-center justify-center rounded-full bg-dry-sage-200"
					>
						<FontAwesomeIcon icon={faTriangleExclamation} class="text-dry-sage-800" />
					</div>
					<span class="text-gray-700">Why is it important?</span>
				</div>
				<HighlightLink href="#" text="View facilitators and hindering factors" />
			</div>
		</div>
		<!-- Right 2/3 steps card -->
		<div class="flex-1 lg:w-2/3">
			<div
				class="rounded-2xl border border-dry-sage-200 bg-gradient-to-br from-dry-sage-50 to-dry-sage-100 p-6 shadow-md shadow-dry-sage-100"
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

<section class="container m-auto mt-12">
	<div class="flex items-center gap-8 lg:flex-row">
		<!-- Left 1/3 title -->
		<div class="w-full space-y-6 lg:w-1/3">
			<h2
				class="text-left text-2xl leading-tight font-bold text-gray-800 text-shadow-dry-sage-200 text-shadow-xs"
			>
				Core Competencies for Equitable Partnership
			</h2>
		</div>
		<!-- Right 2/3 competencies list -->
		<div class="flex-1 lg:w-2/3">
			<div
				class="rounded-2xl border border-dry-sage-200 bg-gradient-to-br from-dry-sage-50 to-dry-sage-100 p-6 shadow-md shadow-dry-sage-100"
			>
				<div class="space-y-4">
					<div class="flex items-center gap-3 p-4 text-base">
						<div
							class="flex h-10 w-10 shrink-0 items-center justify-center rounded-full bg-dry-sage-200"
						>
							<FontAwesomeIcon icon={faScaleBalanced} class="text-dry-sage-800" />
						</div>
						<span class="flex-1 leading-relaxed text-gray-700">
							Capacity to interpret and respond to individual and relational identity, connection,
							uniqueness and inequities
						</span>
					</div>
					<div class="flex items-center gap-3 p-4 text-base">
						<div
							class="flex h-10 w-10 shrink-0 items-center justify-center rounded-full bg-dry-sage-200"
						>
							<FontAwesomeIcon icon={faHandshake} class="text-dry-sage-800" />
						</div>
						<span class="flex-1 leading-relaxed text-gray-700">
							Ability of communities and partners to work in the most suitable, inclusive and
							synergistic way
						</span>
					</div>
					<div class="flex items-center gap-3 p-4 text-base">
						<div
							class="flex h-10 w-10 shrink-0 items-center justify-center rounded-full bg-dry-sage-200"
						>
							<FontAwesomeIcon icon={faArrowsRotate} class="text-dry-sage-800" />
						</div>
						<span class="flex-1 leading-relaxed text-gray-700">
							Aptitude for generating safe and inclusive spaces for multidirectional knowledge and
							skills exchange
						</span>
					</div>
					<div class="flex items-center gap-3 p-4 text-base">
						<div
							class="flex h-10 w-10 shrink-0 items-center justify-center rounded-full bg-dry-sage-200"
						>
							<FontAwesomeIcon icon={faPersonChalkboard} class="text-dry-sage-800" />
						</div>
						<span class="flex-1 leading-relaxed text-gray-700">
							Expertise in democratic leadership and/or facilitation to balance competing priorities
							and ensure shared decision-making
						</span>
					</div>
					<div class="flex items-center gap-3 p-4 text-base">
						<div
							class="flex h-10 w-10 shrink-0 items-center justify-center rounded-full bg-dry-sage-200"
						>
							<FontAwesomeIcon icon={faClipboardCheck} class="text-dry-sage-800" />
						</div>
						<span class="flex-1 leading-relaxed text-gray-700">
							Capacity to analyse readiness for action, successes and areas for improvements
							throughout the research process
						</span>
					</div>
				</div>
			</div>
		</div>
	</div>
</section>

<div class="mx-auto flex max-w-[1400px] flex-col items-stretch justify-center gap-2 lg:flex-row">
	<div
		class="flex min-w-[250px] flex-1 flex-col items-center rounded-3xl border border-gray-300 bg-[#dceadd] p-4 shadow-sm"
	>
		<h2 class="mb-6 text-xl font-bold text-gray-800">Contexts</h2>

		<div class="relative flex w-full flex-grow flex-col items-center justify-center gap-4">
			<div class="flex w-full justify-between px-2">
				<div
					class="z-10 flex h-24 w-24 flex-col items-center justify-center rounded-full border-2 border-[#5e7d62] bg-[#c8dec9] p-2 text-center shadow-sm"
				>
					<span class="text-xs leading-tight font-bold">Social <br />& Structural</span>
				</div>
				<div
					class="z-10 flex h-24 w-24 flex-col items-center justify-center rounded-full border-2 border-[#5e7d62] bg-[#c8dec9] p-2 text-center shadow-sm"
				>
					<span class="text-xs leading-tight font-bold">Political <br />& Policy</span>
				</div>
			</div>

			<div
				class="z-20 my-[-10px] flex h-28 w-28 flex-col items-center justify-center rounded-full border-2 border-[#4a634e] bg-[#7b9c7f] p-2 text-center text-white shadow-md"
			>
				<span class="leading-tight font-bold">Health<br />Issue<br />Importance</span>
			</div>

			<div class="flex w-full justify-between px-2">
				<div
					class="z-10 flex h-24 w-24 flex-col items-center justify-center rounded-full border-2 border-[#5e7d62] bg-[#c8dec9] p-2 text-center shadow-sm"
				>
					<span class="text-xs leading-tight font-bold">Capacity <br />& Readiness</span>
				</div>
				<div
					class="z-10 flex h-24 w-24 flex-col items-center justify-center rounded-full border-2 border-[#5e7d62] bg-[#c8dec9] p-2 text-center shadow-sm"
				>
					<span class="text-xs leading-tight font-bold">Collaboration <br />Trust & Mistrust</span>
				</div>
			</div>

			<svg
				class="pointer-events-none absolute inset-0 z-0 h-full w-full opacity-40"
				style="top:0; left:0;"
			>
				<line x1="25%" y1="15%" x2="50%" y2="50%" stroke="black" stroke-dasharray="4" />
				<line x1="75%" y1="15%" x2="50%" y2="50%" stroke="black" stroke-dasharray="4" />
				<line x1="25%" y1="85%" x2="50%" y2="50%" stroke="black" stroke-dasharray="4" />
				<line x1="75%" y1="85%" x2="50%" y2="50%" stroke="black" stroke-dasharray="4" />
			</svg>
		</div>
	</div>

	<div class="flex items-center justify-center py-2 lg:w-12 lg:py-0">
		<svg
			class="h-8 w-8 rotate-90 transform text-gray-400 lg:rotate-0"
			fill="currentColor"
			viewBox="0 0 20 20"
		>
			<path
				d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z"
			/>
		</svg>
	</div>

	<div
		class="flex min-w-[300px] flex-1 flex-col rounded-3xl border border-gray-300 bg-[#f7ebd6] p-4 shadow-sm"
	>
		<h2 class="mb-4 text-center text-xl font-bold text-gray-800">Partnership Processes</h2>

		<div class="relative flex h-full flex-col gap-4">
			<div class="flex items-start justify-between gap-2">
				<div
					class="flex w-1/2 items-center justify-center rounded-lg border border-[#b8a68e] bg-[#dccbb1] p-2 text-center text-xs font-bold shadow-sm"
				>
					Individual<br />Characteristics
				</div>
				<div class="w-1/2 rounded-lg border border-[#b8a68e] bg-[#dccbb1] p-2 text-xs shadow-sm">
					<div class="mb-1 text-center font-bold">Relationships</div>
					<ul class="list-inside list-disc space-y-1 text-[10px] leading-3">
						<li>Conflict Resolution</li>
						<li>Dialogue/Listening</li>
						<li>Leadership</li>
						<li>Trust</li>
					</ul>
				</div>
			</div>

			<div class="my-2 flex justify-center">
				<div
					class="z-10 w-2/3 rounded-lg border border-[#b8a68e] bg-[#dccbb1] p-3 text-center font-bold shadow-sm"
				>
					Partnership Structures
				</div>
			</div>

			<div class="relative mt-auto flex flex-col items-center gap-2">
				<svg class="pointer-events-none absolute inset-0 z-0 h-full w-full opacity-40">
					<line x1="20%" y1="20%" x2="50%" y2="0%" stroke="black" stroke-dasharray="3" />
					<line x1="80%" y1="20%" x2="50%" y2="0%" stroke="black" stroke-dasharray="3" />
					<line x1="50%" y1="40%" x2="50%" y2="0%" stroke="black" stroke-dasharray="3" />
				</svg>

				<div class="z-10 grid w-full grid-cols-2 gap-x-8 gap-y-2 text-center text-xs font-semibold">
					<div class="rounded border border-[#c4b399] bg-[#e6d6bc] px-2 py-1">CBOs</div>
					<div class="rounded border border-[#c4b399] bg-[#e6d6bc] px-2 py-1">Agency</div>
				</div>

				<div class="z-10 rounded border border-[#b8a68e] bg-[#dccbb1] px-6 py-1 text-xs font-bold">
					Funders
				</div>

				<div class="z-10 grid w-full grid-cols-2 gap-x-8 gap-y-2 text-center text-xs font-semibold">
					<div class="rounded border border-[#c4b399] bg-[#e6d6bc] px-2 py-1">Community</div>
					<div class="rounded border border-[#c4b399] bg-[#e6d6bc] px-2 py-1">Academic</div>
				</div>

				<div class="z-10 grid w-full grid-cols-2 gap-x-4 gap-y-2 text-center text-xs font-semibold">
					<div class="rounded border border-[#c4b399] bg-[#e6d6bc] px-2 py-1">Government</div>
					<div class="rounded border border-[#c4b399] bg-[#e6d6bc] px-2 py-1">Health Care</div>
				</div>
			</div>
		</div>
	</div>

	<div class="flex items-center justify-center py-2 lg:w-12 lg:py-0">
		<svg
			class="h-8 w-8 rotate-90 transform text-gray-400 lg:rotate-0"
			fill="currentColor"
			viewBox="0 0 20 20"
		>
			<path
				d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z"
			/>
		</svg>
	</div>

	<div
		class="flex min-w-[300px] flex-1 flex-col rounded-3xl border border-gray-300 bg-[#fef6d0] p-4 shadow-sm"
	>
		<h2 class="mb-1 text-center text-xl font-bold text-gray-800">Intervention <br />& Research</h2>

		<div class="mt-2 grid h-full grid-cols-2 gap-4">
			<div class="text-center font-serif text-lg italic">Processes</div>
			<div class="text-center font-serif text-lg italic">Outputs</div>

			<div
				class="flex aspect-[4/3] items-center justify-center rounded-lg border border-[#e3d088] bg-[#fceeb5] p-2 text-center text-xs font-bold shadow-sm"
			>
				Integrate<br />Community<br />Knowledge
			</div>
			<div
				class="flex aspect-[4/3] items-center justify-center rounded-lg border border-[#e3d088] bg-[#fceeb5] p-2 text-center text-xs font-bold shadow-sm"
			>
				Culture-<br />Centered<br />Interventions
			</div>

			<div
				class="flex aspect-[4/3] items-center justify-center rounded-lg border border-[#e3d088] bg-[#fceeb5] p-2 text-center text-xs font-bold shadow-sm"
			>
				Empowering<br />Processes
			</div>
			<div
				class="flex aspect-[4/3] items-center justify-center rounded-lg border border-[#e3d088] bg-[#fceeb5] p-2 text-center text-xs font-bold shadow-sm"
			>
				Partnership<br />Synergy
			</div>

			<div
				class="flex aspect-[4/3] items-center justify-center rounded-lg border border-[#e3d088] bg-[#fceeb5] p-2 text-center text-xs font-bold shadow-sm"
			>
				Community<br />Involved in<br />Research
			</div>
			<div
				class="flex aspect-[4/3] items-center justify-center rounded-lg border border-[#e3d088] bg-[#fceeb5] p-2 text-center text-xs font-bold shadow-sm"
			>
				Appropriate<br />Research<br />Design
			</div>
		</div>
	</div>

	<div class="flex items-center justify-center py-2 lg:w-12 lg:py-0">
		<svg
			class="h-8 w-8 rotate-90 transform text-gray-400 lg:rotate-0"
			fill="currentColor"
			viewBox="0 0 20 20"
		>
			<path
				d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z"
			/>
		</svg>
	</div>

	<div
		class="flex min-w-[250px] flex-1 flex-col rounded-3xl border border-gray-300 bg-[#f0dccb] p-4 shadow-sm"
	>
		<h2 class="mb-4 text-center text-xl font-bold text-gray-800">Outcomes</h2>

		<div class="flex h-full flex-col gap-4">
			<div class="flex h-1/2 flex-col">
				<div class="rounded-t-lg bg-[#cd9a77] py-1 text-center text-sm font-bold text-white">
					Intermediate
				</div>
				<div class="flex-grow rounded-b-lg border-x border-b border-[#cd9a77]/30 bg-[#e6cbb4] p-3">
					<ul class="list-inside list-disc space-y-2 text-xs leading-tight text-gray-900">
						<li>Policy Environment</li>
						<li>Sustained Partnership</li>
						<li>Empowerment</li>
						<li>Shared Power Relations in Research</li>
						<li>Cultural Reinforcement</li>
						<li>Individual / Agency Capacity</li>
						<li>Research Productivity</li>
					</ul>
				</div>
			</div>

			<div class="flex h-auto flex-col">
				<div class="rounded-t-lg bg-[#cd9a77] py-1 text-center text-sm font-bold text-white">
					Long-term
				</div>
				<div class="flex-grow rounded-b-lg border-x border-b border-[#cd9a77]/30 bg-[#e6cbb4] p-3">
					<ul class="list-inside list-disc space-y-2 text-xs leading-tight text-gray-900">
						<li>Community Transformation</li>
						<li>Social Justice</li>
						<li>Health / Health Equity</li>
					</ul>
				</div>
			</div>
		</div>
	</div>
</div>
