<script>
	import Card from '$lib/components/Card.svelte';
	import List from '$lib/components/List.svelte';
	import ListBlock from '$lib/components/ListBlock.svelte';
	import ListItem from '$lib/components/ListItem.svelte';
	import { faArrowsLeftRight } from '@fortawesome/free-solid-svg-icons';
	import { FontAwesomeIcon } from '@fortawesome/svelte-fontawesome';
</script>

<svelte:head>
	<title>Trust Building</title>
</svelte:head>

<div class="my-12 flex flex-col items-center space-y-12">
	<section class="container px-8">
		<h1 class="text-4xl font-bold text-gray-800 text-shadow-cornsilk-200 text-shadow-xs">
			Trust Building
		</h1>
	</section>

	<section class="container flex items-start justify-center gap-20">
		<Card theme="dry-sage" class="w-120">
			<h2 class="text-xl font-bold text-dry-sage-700">Trust Dimensions/Content Areas</h2>
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
		</Card>

		<div class="space-y-20">
			<Card theme="cornsilk" class="w-120">
				<h2 class="text-xl font-bold text-cornsilk-900">
					Characteristics of Trustworthy Researchers
				</h2>
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
					<ListItem><strong>Humble:</strong> assumes own importance no more than others</ListItem>
					<ListItem theme="cornsilk">
						<strong>Respectful:</strong> regards others and their perspectives as valuable
					</ListItem>
				</List>
			</Card>

			<Card theme="light-bronze" class="w-120">
				<h2 class="text-xl font-bold text-light-bronze-900">
					Strategies to Enhance and Engender Trust
				</h2>
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
			</Card>
		</div>

		<div class="absolute top-175 rotate-45 text-2xl text-gray-700">
			<FontAwesomeIcon icon={faArrowsLeftRight} />
		</div>
		<div class="absolute top-130 ml-135 rotate-90 text-2xl text-gray-700">
			<FontAwesomeIcon icon={faArrowsLeftRight} />
		</div>
	</section>
</div>
