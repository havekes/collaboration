<script>
	import Blockquote from '$lib/components/Blockquote.svelte';
	import Card from '$lib/components/Card.svelte';
	import CardTitle from '$lib/components/CardTitle.svelte';
	import List from '$lib/components/List.svelte';
	import ListItem from '$lib/components/ListItem.svelte';
	import LongArrow from '$lib/components/LongArrow.svelte';
	import ReferenceLink from '$lib/components/ReferenceLink.svelte';
</script>

<svelte:head>
	<title>Collaborative Alignment: 4-P Foundation</title>
</svelte:head>

<div class="my-8 flex flex-col items-center space-y-8">
	<section class="container mb-8">
		<h1 class="text-3xl font-bold text-cornsilk-800">Collaborative Alignment: 4-P Foundation</h1>
	</section>

	<section class="container">
		<div class="rounded-lg bg-cornsilk-100 p-6">
			<h2 class="text-lg font-bold text-cornsilk-700">
				When collaboration works, key signs of alignment include:
			</h2>
			<List>
				<div class="mt-2 grid grid-cols-2 gap-2">
					<ListItem theme="cornsilk">Measurable progress toward shared objectives</ListItem>
					<ListItem theme="cornsilk">High participant satisfaction and engagement</ListItem>
					<ListItem theme="cornsilk">Meeting or exceeding expectations</ListItem>
					<ListItem theme="cornsilk">Clear, visible achievements</ListItem>
				</div>
			</List>
		</div>
	</section>

	<section class="container text-sm">
		<div class="grid grid-cols-3 gap-x-10">
			<Card theme="cornsilk" class="justify-self-start">
				<CardTitle theme="cornsilk">Purpose</CardTitle>
				<div class="flex-1">
					<List title="The &quot;Why&quot; That Unites Us: the vision & glue for the team">
						<ListItem theme="cornsilk">Provides clarity and direction</ListItem>
						<ListItem theme="cornsilk">
							Attracts committed individuals who share values and goals.
						</ListItem>
						<ListItem theme="cornsilk">
							Serves as a constant reference point for decisions and actions.
						</ListItem>
						<ListItem theme="cornsilk">
							All collaborative efforts begin and should return to the purpose.
						</ListItem>
					</List>
				</div>
				<Blockquote>People invest time when they believe in what’s possible together.</Blockquote>
			</Card>
			<div>
				<LongArrow class="m-auto my-10 h-10 w-20 text-light-bronze-500" />
				<Card theme="light-bronze">
					<List title="Are people aligned with the purpose?">
						<ListItem theme="light-bronze">Has the purpose been clearly communicated?</ListItem>
						<ListItem theme="light-bronze">Are any participants ideologically opposed?</ListItem>
						<ListItem theme="light-bronze">
							Do any organizations feel threatened by the mission?
						</ListItem>
					</List>
				</Card>
			</div>
			<Card theme="cornsilk" class="justify-self-end">
				<CardTitle theme="cornsilk">People</CardTitle>
				<List title="The Energy Behind the Vision: if purpose gives vision, people give life">
					<ListItem theme="cornsilk">Diversity fuels creativity and innovation.</ListItem>
					<ListItem theme="cornsilk">
						Shared vision unites, but differences strengthen outcomes.
					</ListItem>
					<ListItem theme="cornsilk">
						Collaboration thrives when individuals bring unique perspectives, skills, and
						experiences.
					</ListItem>
					<ListItem theme="cornsilk">
						Emotional investment grows when people feel heard and valued .
					</ListItem>
				</List>
				<Blockquote>
					It’s not monoliths that create change — it’s mosaic teams working together.
				</Blockquote>
			</Card>

			<div class="flex items-center gap-6">
				<LongArrow class="m-auto h-10 w-20 shrink-0 rotate-90 text-light-bronze-500" />
				<Card theme="light-bronze">
					<List title="Do results serve the original purpose?">
						<ListItem theme="light-bronze">
							Does each product contribute to the long-term vision?
						</ListItem>
						<ListItem theme="light-bronze">Are we solving root causes, not just symptoms?</ListItem>
					</List>
				</Card>
			</div>
			<div>
				<div class="flex justify-end">
					<LongArrow class="rotate my-5 h-10 w-20 -rotate-30 text-light-bronze-500" />
				</div>
				<Card theme="light-bronze">
					<List title="Do people have what it takes to deliver?">
						<ListItem theme="light-bronze">
							Do participants possess the needed skills and experience?
						</ListItem>
						<ListItem theme="light-bronze">
							Are there strong linkages to external authority or decision-makers?
						</ListItem>
					</List>
				</Card>
				<LongArrow class="rotate my-5 h-10 w-20 -rotate-30 text-light-bronze-500" />
			</div>
			<div class="flex items-center gap-6">
				<Card theme="light-bronze">
					<List title="Are people aligned with the process?">
						<ListItem theme="light-bronze">Is there buy-in to the group’s operating rules?</ListItem
						>
						<ListItem theme="light-bronze">Are roles and responsibilities clear?</ListItem>
						<ListItem theme="light-bronze">
							Has leadership been assigned and empowered effectively?
						</ListItem>
					</List>
				</Card>
				<LongArrow class="m-auto h-10 w-20 shrink-0 -rotate-90 text-light-bronze-500" />
			</div>

			<Card theme="cornsilk" class="justify-self-end">
				<CardTitle theme="cornsilk">Product</CardTitle>
				<List title="The Tangible Outcomes That Prove Progress: without results, attention fades">
					<ListItem theme="cornsilk">Deliverables must be meaningful and measurable .</ListItem>
					<ListItem theme="cornsilk">
						Milestones celebrate progress and sustain motivation.
					</ListItem>
					<ListItem theme="cornsilk">
						Outcomes should directly advance the original purpose.
					</ListItem>
					<ListItem theme="cornsilk">Regular evaluation ensures relevance and impact.</ListItem>
				</List>
				<Blockquote>Without results, attention fades.</Blockquote>
			</Card>
			<div class="flex flex-col-reverse">
				<LongArrow class="m-auto my-10 h-10 w-20 text-light-bronze-500" />
				<Card theme="light-bronze">
					<List title="Does the process support real results?">
						<ListItem theme="light-bronze">Are resources adequate (time, funding, tools)?</ListItem>
						<ListItem theme="light-bronze">Are deadlines realistic and flexible?</ListItem>
						<ListItem theme="light-bronze">Is there space for learning and adaptation?</ListItem>
					</List>
				</Card>
			</div>
			<Card theme="cornsilk" class="justify-self-start">
				<CardTitle theme="cornsilk">Process</CardTitle>
				<List title="The &quot;How&quot; We Work Together: process becomes the road map">
					<ListItem theme="cornsilk">
						Governance structures guide decision-making and behavior.
					</ListItem>
					<ListItem theme="cornsilk">
						Includes meeting logistics, roles, facilitation, and conflict resolution.
					</ListItem>
					<ListItem theme="cornsilk">
						Prevents chaos by honoring both unity and individuality.
					</ListItem>
					<ListItem theme="cornsilk">
						Ongoing refinement ensures fairness and effectiveness.
					</ListItem>
				</List>
				<Blockquote>
					“The uniqueness of people provides richness in the diversity of ideas and opinions as they
					strive together for a shared purpose and vision. That same uniqueness and individuality,
					however, can provide an environment for disagreement, divisiveness, and chaos.” (Walker et
					al., 2023, p. 5)
				</Blockquote>
			</Card>
		</div>
	</section>

	<section class="container text-center">
		<ReferenceLink theme="cornsilk" refs={[{ name: 'Walker et al. (2023)', link: '' }]} />
	</section>
</div>
