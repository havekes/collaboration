<script>
	import Card from '$lib/components/Card.svelte';
	import CardTitle from '$lib/components/CardTitle.svelte';
	import List from '$lib/components/List.svelte';
	import ListItem from '$lib/components/ListItem.svelte';
	import LongArrow from '$lib/components/LongArrow.svelte';
	import { faArrowRightLong, faArrowsLeftRight } from '@fortawesome/free-solid-svg-icons';
	import { FontAwesomeIcon } from '@fortawesome/svelte-fontawesome';
</script>

<div class="my-12 flex flex-col items-center space-y-12">
	<section class="container px-8">
		<h1 class="text-4xl font-bold text-gray-800 text-shadow-cornsilk-200 text-shadow-xs">
			Collaborative alignment: 4-P Foundation
		</h1>
	</section>

	<section class="container px-8">
		<Card theme="dry-sage">
			<h2 class="text-lg font-bold text-dry-sage-700">
				When collaboration works, key signs of alignment include:
			</h2>
			<List>
				<ListItem>Measurable progress toward shared objectives</ListItem>
				<ListItem>High participant satisfaction and engagement</ListItem>
				<ListItem>Meeting or exceeding expectations</ListItem>
				<ListItem>Clear, visible achievements</ListItem>
			</List>
		</Card>
	</section>

	<section class="container">
		<div class="grid grid-cols-2 gap-24 px-8">
			<Card theme="cornsilk" class="justify-self-start">
				<CardTitle theme="cornsilk">Purpose</CardTitle>
				<List title="The &quot;Why&quot; That Unites Us: the vision & glue for the team">
					<ListItem theme="cornsilk">Provides clarity and direction</ListItem>
					<ListItem theme="cornsilk">
						Attracts committed individuals who share values and goals
					</ListItem>
					<ListItem theme="cornsilk">
						Serves as a constant reference point for decisions and actions
					</ListItem>
					<ListItem theme="cornsilk">
						All collaborative efforts begin and should return to the purpose
					</ListItem>
				</List>
				<blockquote
					class="rounded-lg border border-cornsilk-300 p-4 text-gray-800 italic shadow-cornsilk-100"
				>
					People invest time when they believe in what’s possible together.
				</blockquote>
			</Card>
			<Card theme="cornsilk" class="justify-self-end">
				<CardTitle theme="cornsilk">People</CardTitle>
			</Card>
			<Card theme="cornsilk" class="justify-self-start">
				<CardTitle theme="cornsilk">Process</CardTitle>
			</Card>
			<Card theme="cornsilk" class="justify-self-end">
				<CardTitle theme="cornsilk">Product</CardTitle>
			</Card>
		</div>
		<LongArrow class="h-10 w-20 text-cornsilk-800" />
		<LongArrow class="h-10 w-20 text-cornsilk-800" />
		<LongArrow class="h-10 w-20 text-cornsilk-800" />
		<LongArrow class="h-10 w-20 text-cornsilk-800" />
	</section>
</div>
