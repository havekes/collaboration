<script>
	import List from '$lib/components/List.svelte';
	import ListBlock from '$lib/components/ListBlock.svelte';
	import ListItem from '$lib/components/ListItem.svelte';
	import PageTitle from '$lib/components/PageTitle.svelte';
	import StickyTitle from '$lib/components/StickyTitle.svelte';
</script>

<svelte:head>
	<title>Facilitating & Hindering Factors to the Success of Partnership</title>
</svelte:head>

<div class="flex flex-col items-center">
	<StickyTitle>Interpersonal Qualities</StickyTitle>

	<section class="container mb-8">
		<div class="grid grid-cols-2 gap-8">
			<ListBlock title="Facilitating Factors" theme="cornsilk">
				<List title="Shared vision, goals and/or mission">
					<ListItem>Provides a unified direction for all partners.</ListItem>
					<ListItem>Ensures alignment and collective purpose in collaborative efforts.</ListItem>
					<ListItem>
						<strong><a href="/collaborative-alignment">See: 4-P Foundation</a></strong>
					</ListItem>
				</List>
				<List title="Trust between partners">
					<ListItem>Foundational for equitable collaboration.</ListItem>
					<ListItem>
						Trust enables open communication, shared decision-making, and sustained engagement
					</ListItem>
					<ListItem>
						<strong><a href="/trust">Learn more linking to Building Trust page</a></strong>
					</ListItem>
				</List>
				<List title="Respect among partners">
					<ListItem>Recognizes and values diverse contributions and perspectives.</ListItem>
					<ListItem>
						Requires careful selection of participants to ensure inclusivity and equity (Newcomb et
						al., 2021, p. 136).
					</ListItem>
				</List>
				<List title="Mutual benefit for all partners">
					<ListItem>
						All partners should derive tangible or intangible value from the collaboration.
					</ListItem>
					<ListItem>
						Requires equitable distribution of benefits and shared ownership of outcomes.
					</ListItem>
				</List>
				<List title="Good relationship between partners">
					<ListItem>Characterized by genuineness, trust, and respect.</ListItem>
					<ListItem>Requires dedicated time and ongoing engagement to develop and sustain</ListItem>
				</List>
				<List title="Effective conflict resolution">
					<ListItem>Proactive strategies for managing disagreements are essential.</ListItem>
					<ListItem>Preserves partnership integrity and fosters constructive dialogue.</ListItem>
				</List>
			</ListBlock>

			<ListBlock title="Hindering Factors" theme="dry-sage">
				<List title="Mistrust between partners">
					<ListItem>
						May result from historical inequities, lack of transparency, or power imbalances.
					</ListItem>
					<ListItem>
						Address by promoting transparency, openness, accountability, and inclusive practices.
					</ListItem>
				</List>
				<List title="Inconsistent partner participation/membership">
					<ListItem
						>Can be caused by competing interests, priorities, or organizational demands.</ListItem
					>
					<ListItem>Can weaken collaboration and erode trust over time.</ListItem>
				</List>
				<List title="Lack of shared vision, goals, and/or mission">
					<ListItem>Leads to misaligned goals and fragmented efforts.</ListItem>
					<ListItem>Regularly revisit and reaffirm shared mission and objectives.</ListItem>
				</List>
				<List title="Lack of mutual benefits">
					<ListItem
						>Partnership sustainability declines when benefits are perceived as unequal.</ListItem
					>
				</List>
			</ListBlock>
		</div>
	</section>

	<StickyTitle>Operational Proceses</StickyTitle>

	<section class="container mb-8">
		<div class="grid grid-cols-2 gap-8">
			<ListBlock title="Facilitating Factors" theme="cornsilk">
				<List title="Positive community impact">
					<ListItem>Shared decision-making power with communities</ListItem>
					<ListItem>Communities empowered to lead or co-lead initiatives</ListItem>
					<ListItem>
						Enhanced motivation for collaboration due to visible, meaningful outcomes (Bustos et
						al., 2024, p. 8)
					</ListItem>
				</List>
				<List title="Bringing together diverse stakeholders">
					<ListItem>
						Intentional inclusion of varied actors (e.g., community members, NGOs, academics,
						policymakers)
					</ListItem>
					<ListItem
						>Valuing diverse perspectives to enrich project design and implementation</ListItem
					>
				</List>
				<List title="High-quality leadership">
					<ListItem
						>Decentralized leadership models that distribute power and responsibilities</ListItem
					>
					<ListItem>Emphasis on shared leadership to leverage diverse skills and expertise</ListItem
					>
					<ListItem>Leaders who listen first and prioritize community input</ListItem>
					<ListItem
						>Trusted individuals with strong reputations, fostering credibility and trust</ListItem
					>
				</List>
				<List title="Well-structured meeting">
					<ListItem>Clear agendas, defined objectives, and inclusive participation</ListItem>
					<ListItem>Timely follow-ups and documentation</ListItem>
					<ListItem>Safe spaces for open dialogue and decision-making</ListItem>
				</List>
				<List title="Careful initial selection of partners">
					<ListItem>Strategic alignment of mission, values, and capacity</ListItem>
					<ListItem>
						Assessment of potential partners' reliability, expertise, and commitment to equity
					</ListItem>
				</List>
				<List title="Clearly defined roles and responsibilities">
					<ListItem>Transparent delineation of tasks, expectations, and accountability</ListItem>
					<ListItem>Reduces overlap and confusion; enhances efficiency and trust</ListItem>
					<ListItem>
						<strong
							><a href="/rolefulness">Learn more linking to Building Rolefulness page</a></strong
						>
					</ListItem>
				</List>
			</ListBlock>
			<ListBlock title="Hindering Factors" theme="dry-sage">
				<List title="Excessive time commitment & High burden of activities/tasks">
					<ListItem>
						High demands on participants' time, especially volunteers or community members
					</ListItem>
					<ListItem>Risk of burnout and reduced engagement over time</ListItem>
					<ListItem>Unequal distribution of workload across partners</ListItem>
				</List>
				<List title="Unclear roles and responsibilities">
					<ListItem>
						<strong
							><a href="/rolefulness">Learn more linking to Building Rolefulness page</a></strong
						>
					</ListItem>
				</List>
				<List title="Differing expectations of partners">
					<ListItem>Misalignment in goals, timelines, or desired outcomes</ListItem>
					<ListItem>
						Can result in frustration, power struggles, and reduced collaboration effectiveness
					</ListItem>
				</List>
				<List title="Poor or unequal decision-making">
					<ListItem>Researchers needs to ensure decentralized decision processes.</ListItem>
				</List>
				<List title="Excessive funding pressures or funding control struggles">
					<ListItem>Short-term funding cycles disrupting long-term collaboration</ListItem>
					<ListItem>Power imbalances when funders dictate terms without community input</ListItem>
				</List>
			</ListBlock>
		</div>
	</section>

	<StickyTitle>Network Processes</StickyTitle>

	<section class="container">
		<div class="grid grid-cols-2 gap-8">
			<ListBlock title="Facilitating Factors" theme="cornsilk">
				<List title="Exchanging information and knowledge">
					<ListItem>Sharing insights, data, and expertise across partners</ListItem>
					<ListItem>Promoting mutual learning and informed decision-making</ListItem>
				</List>
				<List title="Sharing resources">
					<ListItem>Ensuring equitable access to support collaboration goals</ListItem>
				</List>
				<List title="Effective and frequent communication">
					<ListItem>Clearly defining roles, expectations, and priorities upfront</ListItem>
					<ListItem>Maintaining transparency and alignment with shared mission</ListItem>
					<ListItem>Building trust through bidirectional dialogue</ListItem>
					<ListItem>Supporting reconciliation-oriented partnership development</ListItem>
					<ListItem
						><strong><a href="/best-practices#communication">Learn more</a></strong></ListItem
					>
				</List>
				<List title="Informal relationship created">
					<ListItem
						>Developing personal rapport and shared understanding beyond formal agreements</ListItem
					>
				</List>
			</ListBlock>
			<ListBlock title="Hindering Factors" theme="dry-sage">
				<List title="Poor communication between partners">
					<ListItem>Create a Road Map to align goals and timelines.</ListItem>
					<ListItem
						><strong><a href="/best-practices#communication">Learn more</a></strong></ListItem
					>
				</List>
				<List title="Lack of a common knowledge or shared terms between partners">
					<ListItem>Risk of misrepresentation or inaccurate portrayal of community needs</ListItem>
					<ListItem>
						Highlights oppressive structures in academic language; calls for intentional, inclusive
						dialogue to reduce barriers (Bustos et al., 2024, p. 9)
					</ListItem>
				</List>
			</ListBlock>
		</div>
	</section>
</div>
