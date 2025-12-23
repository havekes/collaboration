<script>
	import picture2 from '$lib/assets/images/Picture2.png';
	import Blockquote from '$lib/components/Blockquote.svelte';
	import Card from '$lib/components/Card.svelte';
	import CardTitle from '$lib/components/CardTitle.svelte';
	import List from '$lib/components/List.svelte';
	import ListItem from '$lib/components/ListItem.svelte';
	import ReferenceLink from '$lib/components/ReferenceLink.svelte';
	import { faArrowsLeftRight } from '@fortawesome/free-solid-svg-icons';
	import { FontAwesomeIcon } from '@fortawesome/svelte-fontawesome';
</script>

<svelte:head>
	<title>Trust Building</title>
</svelte:head>

<div class="my-8 flex flex-col items-center space-y-12">
	<section class="container mb-8">
		<h1 class="text-3xl font-bold text-light-bronze-800">Trust Building</h1>
	</section>
	<section class="container flex items-start justify-center gap-20">
		<Card theme="dry-sage" class="w-1/2 min-w-120">
			<CardTitle theme="dry-sage">Trust Dimensions/Content Areas</CardTitle>
			<List>
				<ListItem>
					<strong>Honesty<sup>*</sup>:</strong> Integrity and openness in a relationship
				</ListItem>
				<ListItem>
					<strong>Communication<sup>*</sup>:</strong> Quality and nature of information exchange
				</ListItem>
				<ListItem>
					<strong>Confidence<sup>*</sup>:</strong> Belief in reliability of parties
				</ListItem>
				<ListItem>
					<strong>Confidentiality:</strong> Maintaining privacy of personal information
				</ListItem>
				<ListItem>
					<strong>Competence:</strong> Qualifications, reputation, and perceived ability to provide services
				</ListItem>
				<ListItem>
					<strong>Fairness*:</strong> Perceived treatment of disadvantaged and vulnerable groups
				</ListItem>
				<ListItem>
					<strong>Fidelity:</strong> Duty to help partners/participants beyond self-interest
				</ListItem>
				<ListItem><strong>Safety:</strong> Perceived consequences of participation</ListItem>
				<ListItem>
					<strong>System trust:</strong> Belief in institutions, processes and policies of the research
					system
				</ListItem>
			</List>
			<p class="text-sm text-gray-700">
				<sup>*</sup>Dimensions of trust more relevant to patients and community members involved in
				advanced research roles
			</p>
			<ReferenceLink
				theme="cornsilk"
				refs={[{ name: 'Wilkins (2018)', link: '' }]}
				adapted={false}
			/>
		</Card>

		<div class="w-1/2 space-y-20">
			<Card theme="cornsilk" class="w-full">
				<CardTitle theme="cornsilk">Characteristics of Trustworthy Researchers</CardTitle>
				<List>
					<ListItem theme="cornsilk"><strong>Accessible:</strong> easily reached</ListItem>
					<ListItem theme="cornsilk">
						<strong>Approachable:</strong> welcoming, easy to talk to
					</ListItem>
					<ListItem theme="cornsilk">
						<strong>Attentive:</strong> observant, listens carefully; responds to concerns
					</ListItem>
					<ListItem theme="cornsilk">
						<strong>Empathetic:</strong> able to understand others feelings
					</ListItem>
					<ListItem theme="cornsilk"><strong>Honest:</strong> truthful and open</ListItem>
					<ListItem theme="cornsilk">
						<strong>Humble:</strong> assumes own importance no more than others
					</ListItem>
					<ListItem theme="cornsilk">
						<strong>Respectful:</strong> regards others and their perspectives as valuable
					</ListItem>
				</List>

				<ReferenceLink
					theme="cornsilk"
					refs={[{ name: 'Wilkins (2018)', link: '' }]}
					adapted={false}
				/>
			</Card>

			<Card theme="light-bronze" class="w-full">
				<CardTitle theme="light-bronze">Strategies to Enhance and Engender Trust</CardTitle>
				<List>
					<ListItem theme="light-bronze">Balance power dynamics</ListItem>
					<ListItem theme="light-bronze">Be transparent about goals, motivations</ListItem>
					<ListItem theme="light-bronze">
						Create infrastructure and policies to community stakeholders meaningful involvement
					</ListItem>
					<ListItem theme="light-bronze">Develop cultural humility</ListItem>
					<ListItem theme="light-bronze">Equitably distribute resources</ListItem>
					<ListItem theme="light-bronze">Effectively communicate, in all directions</ListItem>
					<ListItem theme="light-bronze">Establish pattern of fulfilling trust</ListItem>
					<ListItem theme="light-bronze">Share decision-making among partners</ListItem>
					<ListItem theme="light-bronze">
						Value different resources and assets (such as the lived experience)
					</ListItem>
				</List>

				<ReferenceLink
					theme="cornsilk"
					refs={[{ name: 'Wilkins (2018)', link: '' }]}
					adapted={false}
				/>
			</Card>
		</div>

		<div class="absolute top-200 rotate-45 text-2xl text-light-bronze-500">
			<FontAwesomeIcon icon={faArrowsLeftRight} />
		</div>
		<div class="absolute top-154 ml-170 rotate-90 text-2xl text-light-bronze-500">
			<FontAwesomeIcon icon={faArrowsLeftRight} />
		</div>
	</section>

	<section class="container">
		<div class="grid grid-cols-2 gap-x-20 gap-y-6 rounded-lg bg-dry-sage-100 py-6">
			<div class="px-8">
				<List title="Factors to consider when building trust:">
					<ListItem>Variability in dimensions of trust</ListItem>
					<ListItem>Characteristics of trustworthy researchers</ListItem>
				</List>
			</div>
			<div class="px-8">
				<List title="Level of trust may be shaped by:">
					<ListItem>Educational attainment</ListItem>
					<ListItem>Cultural beliefs</ListItem>
					<ListItem>Personal and community experiences with research</ListItem>
				</List>
			</div>
			<div class="col-span-2 text-center">
				<ReferenceLink theme="cornsilk" refs={[{ name: 'Wilkins (2018)', link: '' }]} />
			</div>
		</div>
	</section>

	<section class="container flex gap-8">
		<div
			class="flex h-full w-4/7 flex-col items-center justify-center gap-2 rounded-2xl border border-cornsilk-100 bg-cornsilk-50 p-6 shadow-sm shadow-cornsilk-100"
		>
			<img src={picture2} alt="" class="h-auto w-full rounded-xl" />
			<ReferenceLink
				theme="cornsilk"
				refs={[{ name: 'Jagosh et al. (2015)', link: '' }]}
				adapted={false}
			/>
		</div>
		<Card theme="cornsilk" class="w-3/7">
			<CardTitle theme="cornsilk">Trust in Community-based participatory research</CardTitle>
			<Blockquote>
				<strong>Voluntary Trust:</strong> Emerges from close interpersonal relationships; defined as “a
				consensual absence of calculation, where partners voluntarily forego calculating outcomes” (Jagosh
				et al., 2015, p. 9).
			</Blockquote>
			<div class="space-y-2 px-4">
				<List title="What is it built on?">
					<ListItem>Commonality & Reciprocity</ListItem>
				</List>
				<List title="How to build trust?"><span></span></List>
			</div>
			<Blockquote>
				<strong>Example - Trust by Proxy:</strong> Trust developed in one community relationship extends
				to other stakeholders, facilitating broader collaboration.
			</Blockquote>
			<ReferenceLink theme="cornsilk" refs={[{ name: 'Jagosh et al. (2015)', link: '' }]} />
		</Card>
	</section>
</div>
