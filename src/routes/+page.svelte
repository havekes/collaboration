<script lang="ts">
	import picture1 from '$lib/assets/images/Picture1.png';
	import HighlightLink from '$lib/components/HighlightLink.svelte';
	import { FontAwesomeIcon } from '@fortawesome/svelte-fontawesome';
	import {
		faHandsHolding,
		faMagnifyingGlass,
		faTriangleExclamation
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
