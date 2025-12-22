<script>
	import Card from '$lib/components/Card.svelte';
	import CardTitle from '$lib/components/CardTitle.svelte';
	import List from '$lib/components/List.svelte';
	import ListItem from '$lib/components/ListItem.svelte';
	import RoundedIcon from '$lib/components/RoundedIcon.svelte';
	import {
		faArrowRight,
		faArrowRightLong,
		faArrowsLeftRight,
		faBrain,
		faEquals,
		faPeopleGroup,
		faPlus
	} from '@fortawesome/free-solid-svg-icons';
	import { FontAwesomeIcon } from '@fortawesome/svelte-fontawesome';
	import Page from '../competencies/+page.svelte';
	import Blockquote from '$lib/components/Blockquote.svelte';
</script>

<div class="my-8 flex flex-col items-center space-y-8">
	<section class="container">
		<h1 class="text-3xl font-bold text-cornsilk-800">Rolefulness</h1>
	</section>

	<div class="container grid grid-cols-2 gap-8">
		<div>
			<div
				class="space-y-8 rounded-2xl border border-cornsilk-100 bg-white p-8 shadow-sm shadow-cornsilk-100"
			>
				<div class="absolute top-135 left-43 rotate-90 text-xl text-dry-sage-500">
					<FontAwesomeIcon icon={faArrowsLeftRight} />
				</div>
				<section class=" grid grid-cols-2">
					<div class="flex items-center">
						<Card theme="dry-sage" class="w-40 rounded-full py-6 text-center">
							<h2 class="font-bold text-dry-sage-900">Social</h2>
						</Card>
					</div>
					<div class="space-y-4 text-sm text-gray-800">
						<Card theme="dry-sage" class="p-4!">My role is necessary for other people.</Card>
						<Card theme="dry-sage" class="p-4!">I can apply my strong point for society.</Card>
						<Card theme="dry-sage" class="p-4!">I have a role in the group I belong to.</Card>
						<Card theme="dry-sage" class="p-4!">I am useful in society.</Card>
					</div>
					<div class="text-xl text-dry-sage-500">
						<div class="absolute top-70 left-78 -rotate-30">
							<FontAwesomeIcon icon={faArrowRightLong} />
						</div>
						<div class="absolute top-89 left-78 -rotate-6">
							<FontAwesomeIcon icon={faArrowRightLong} />
						</div>
						<div class="absolute top-108 left-78 rotate-16">
							<FontAwesomeIcon icon={faArrowRightLong} />
						</div>
						<div class="absolute top-125 left-78 rotate-30">
							<FontAwesomeIcon icon={faArrowRightLong} />
						</div>
					</div>
				</section>

				<section class="grid grid-cols-2">
					<div class="flex items-center">
						<Card theme="light-bronze" class="w-40 rounded-full py-6 text-center">
							<h2 class="font-bold text-light-bronze-900">Internal</h2>
						</Card>
					</div>
					<div class="space-y-4 text-sm text-gray-800">
						<Card theme="light-bronze" class="p-4!">I realize my individuality by my role.</Card>
						<Card theme="light-bronze" class="p-4!">I am satisfied with my role.</Card>
						<Card theme="light-bronze" class="p-4!">I gain confidence because of my role.</Card>
					</div>
					<div class="text-xl text-light-bronze-500">
						<div class="absolute top-152 left-78 -rotate-24">
							<FontAwesomeIcon icon={faArrowRightLong} />
						</div>
						<div class="absolute top-168 left-78">
							<FontAwesomeIcon icon={faArrowRightLong} />
						</div>
						<div class="absolute top-184 left-78 rotate-24">
							<FontAwesomeIcon icon={faArrowRightLong} />
						</div>
					</div>
				</section>
			</div>
		</div>
		<div class="space-y-8">
			<Card theme="cornsilk">
				<CardTitle theme="cornsilk">From Outside to Inside</CardTitle>
				<RoundedIcon icon={faPeopleGroup} color="cornsilk" colorWeight="300">
					<strong>Social Role</strong> (being part of a group, recognized for your role).
				</RoundedIcon>
				<div class="mr-12 text-center text-xl text-cornsilk-900">
					<FontAwesomeIcon icon={faArrowsLeftRight} class="rotate-90" />
				</div>
				<RoundedIcon icon={faBrain} color="cornsilk" colorWeight="300">
					<strong>Social Role</strong> (being part of a group, recognized for your role).
				</RoundedIcon>
			</Card>
			<Card theme="cornsilk" class="text-gray-800">
				<List>
					<ListItem theme="cornsilk">
						Social rolefulness
						<FontAwesomeIcon icon={faArrowRight} class="text-sm text-cornsilk-900" /> social experiences
						<FontAwesomeIcon icon={faArrowRight} class="text-sm text-cornsilk-900" /> interpersonal communication
					</ListItem>
					<ListItem theme="cornsilk">
						Develop social
						<FontAwesomeIcon icon={faPlus} class="text-sm text-cornsilk-900" /> communication skills
						<FontAwesomeIcon icon={faEquals} class="text-sm text-cornsilk-900" /> establish and maintain
						good relationships with others
					</ListItem>
					<ListItem theme="cornsilk">
						When people communicate well and connect with others, they can more easily step into
						meaningful roles—whether as leaders, teammates, or community members.
					</ListItem>
				</List>
			</Card>
			<Card theme="cornsilk">
				<CardTitle theme="cornsilk">How We Build Self-Worth: It Starts With Connection</CardTitle>
				<div class="flex items-center justify-evenly font-semibold">
					<span>Social Recognition</span>
					<FontAwesomeIcon icon={faArrowRight} class="text-sm text-cornsilk-900" />
					<span>Inner Confidence</span>
				</div>
				<Blockquote>
					When others accept, appreciate, or value us, it shapes how we see ourselves. These
					positive interactions build self-esteem.
				</Blockquote>
			</Card>
		</div>
	</div>
</div>
