<script>
	import Link from '$lib/components/Link.svelte';
	import List from '$lib/components/List.svelte';
	import ListBlock from '$lib/components/ListBlock.svelte';
	import ListItem from '$lib/components/ListItem.svelte';
	import ReferenceLink from '$lib/components/ReferenceLink.svelte';
	import StickyTitle from '$lib/components/StickyTitle.svelte';
</script>

<svelte:head>
	<title>Facilitating & Hindering Factors to the Success of Partnership</title>
</svelte:head>

<div class="my-8 flex flex-col items-center">
	<section class="container mb-8">
		<h1 class="text-3xl font-bold text-light-bronze-800">
			Facilitating & Hindering Factors to the Success of Partnership
		</h1>
	</section>

	<StickyTitle>Interpersonal Qualities</StickyTitle>

	<section class="container mb-8">
		<div class="grid grid-cols-2 gap-8">
			<ListBlock title="Facilitating Factors" theme="cornsilk">
				<List title="Shared vision, goals and/or mission">
					<ListItem theme="cornsilk">Provides a unified direction for all partners.</ListItem>
					<ListItem theme="cornsilk">
						Ensures alignment and collective purpose in collaborative efforts.
					</ListItem>
					<ListItem theme="cornsilk">
						<strong>
							<Link theme="cornsilk" href="/collaborative-alignment">See: 4-P Foundation</Link>
						</strong>
					</ListItem>
				</List>
				<List title="Trust between partners">
					<ListItem theme="cornsilk">Foundational for equitable collaboration.</ListItem>
					<ListItem theme="cornsilk">
						Trust enables open communication, shared decision-making, and sustained engagement.
					</ListItem>
					<ListItem theme="cornsilk">
						<strong>
							<Link theme="cornsilk" href="/trust-building">See: Building Trust</Link>
						</strong>
					</ListItem>
				</List>
				<List title="Respect among partners">
					<ListItem theme="cornsilk">
						Recognizes and values diverse contributions and perspectives.
					</ListItem>
					<ListItem theme="cornsilk">
						Requires careful selection of participants to ensure inclusivity and equity.
					</ListItem>
				</List>
				<List title="Mutual benefit for all partners">
					<ListItem theme="cornsilk">
						All partners should derive tangible or intangible value from the collaboration.
					</ListItem>
					<ListItem theme="cornsilk">
						Requires equitable distribution of benefits and shared ownership of outcomes.
					</ListItem>
				</List>
				<List title="Good relationship between partners">
					<ListItem theme="cornsilk">Characterized by genuineness, trust, and respect.</ListItem>
					<ListItem theme="cornsilk">
						Requires dedicated time and ongoing engagement to develop and sustain
					</ListItem>
				</List>
				<List title="Effective conflict resolution">
					<ListItem theme="cornsilk">
						Proactive strategies for managing disagreements are essential.
					</ListItem>
					<ListItem theme="cornsilk">
						Preserves partnership integrity and fosters constructive dialogue.
					</ListItem>
				</List>
				<ReferenceLink
					theme="cornsilk"
					refs={[
						{ name: 'Bustos et al. (2024)', link: '' },
						{ name: 'Newcomb et al. (2021)', link: '' }
					]}
				/>
			</ListBlock>

			<ListBlock title="Hindering Factors" theme="dry-sage">
				<List title="Mistrust between partners">
					<ListItem>
						May result from historical inequities, lack of transparency, or power imbalances.
					</ListItem>
					<ListItem>
						Address by promoting transparency, openness, accountability, and inclusive practices.
					</ListItem>
					<ListItem>
						<strong>
							<Link theme="dry-sage" href="/trust-building">See: Building trust</Link>
						</strong>
					</ListItem>
				</List>
				<List title="Inconsistent partner participation/membership">
					<ListItem>
						Can be caused by competing interests, priorities, or organizational demands.
					</ListItem>
					<ListItem>Can weaken collaboration and erode trust over time.</ListItem>
				</List>
				<List title="Lack of shared vision, goals, and/or mission">
					<ListItem>Leads to misaligned goals and fragmented efforts.</ListItem>
					<ListItem>Regularly revisit and reaffirm shared mission and objectives.</ListItem>
					<ListItem>
						<strong>
							<Link theme="dry-sage" href="/trust-building">See: Building trust</Link>
						</strong>
					</ListItem>
				</List>
				<List title="Lack of mutual benefits">
					<ListItem>
						Partnership sustainability declines when benefits are perceived as unequal.
					</ListItem>
				</List>
				<ReferenceLink theme="dry-sage" refs={[{ name: 'Bustos et al. (2024)', link: '' }]} />
			</ListBlock>
		</div>
	</section>

	<StickyTitle>Operational Processes</StickyTitle>

	<section class="container mb-8">
		<div class="grid grid-cols-2 gap-8">
			<ListBlock title="Facilitating Factors" theme="cornsilk">
				<List title="Positive community impact">
					<ListItem theme="cornsilk">Shared decision-making power with communities</ListItem>
					<ListItem theme="cornsilk">Communities empowered to lead or co-lead initiatives</ListItem>
					<ListItem theme="cornsilk">
						Enhanced motivation for collaboration due to visible, meaningful outcomes
					</ListItem>
				</List>
				<List title="Bringing together diverse stakeholders">
					<ListItem theme="cornsilk">
						Intentional inclusion of varied actors (e.g., community members, NGOs, academics,
						policymakers)
					</ListItem>
					<ListItem theme="cornsilk">
						Valuing diverse perspectives to enrich project design and implementation
					</ListItem>
					<ListItem theme="cornsilk">
						<strong>
							<Link
								theme="cornsilk"
								href="/competencies#Understanding-Community-Context-to-Work-Synergistically"
							>
								See: Competencies
							</Link>
						</strong>
					</ListItem>
				</List>
				<List title="High-quality leadership">
					<ListItem theme="cornsilk">
						Decentralized leadership models that distribute power and responsibilities
					</ListItem>
					<ListItem theme="cornsilk">
						Emphasis on shared leadership to leverage diverse skills and expertise
					</ListItem>
					<ListItem theme="cornsilk">
						Leaders who listen first and prioritize community input
					</ListItem>
					<ListItem theme="cornsilk">
						Trusted individuals with strong reputations, fostering credibility and trust
					</ListItem>
					<ListItem theme="cornsilk">
						<strong>
							<Link theme="cornsilk" href="/competencies#Co-Leadership-Skills">
								See: Competencies
							</Link>
						</strong>
					</ListItem>
				</List>
				<List title="Well-structured meeting">
					<ListItem theme="cornsilk">
						Clear agendas, defined objectives, and inclusive participation
					</ListItem>
					<ListItem theme="cornsilk">Timely follow-ups and documentation</ListItem>
					<ListItem theme="cornsilk">Safe spaces for open dialogue and decision-making</ListItem>
				</List>
				<List title="Careful initial selection of partners">
					<ListItem theme="cornsilk">Strategic alignment of mission, values, and capacity</ListItem>
					<ListItem theme="cornsilk">
						Assessment of potential partners' reliability, expertise, and commitment to equity
					</ListItem>
				</List>
				<List title="Clearly defined roles and responsibilities">
					<ListItem theme="cornsilk">
						Transparent delineation of tasks, expectations, and accountability
					</ListItem>
					<ListItem theme="cornsilk">
						Reduces overlap and confusion; enhances efficiency and trust
					</ListItem>
					<ListItem theme="cornsilk">
						<strong>
							<Link theme="cornsilk" href="/rolefulness">See: Rolefulness</Link>
						</strong>
					</ListItem>
				</List>
				<ReferenceLink theme="cornsilk" refs={[{ name: 'Bustos et al. (2024)', link: '' }]} />
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
						<strong>
							<Link theme="dry-sage" href="/rolefulness">See: Rolefulness</Link>
						</strong>
					</ListItem>
				</List>
				<List title="Differing expectations of partners">
					<ListItem>Misalignment in goals, timelines, or desired outcomes</ListItem>
					<ListItem>
						Can result in frustration, power struggles, and reduced collaboration effectiveness
					</ListItem>
					<ListItem>
						<strong>
							<Link
								theme="dry-sage"
								href="/best-practices#Establish-Clear-Expectations-and-Common-Understanding"
							>
								See: Best practices
							</Link>
						</strong>
					</ListItem>
				</List>
				<List title="Poor or unequal decision-making">
					<ListItem>Researchers need to ensure decentralized decision processes.</ListItem>
					<ListItem>
						<strong>
							<Link theme="dry-sage" href="/best-practices#Promote-Equitable-Decision-Making">
								See: Best practices
							</Link>
						</strong>
					</ListItem>
				</List>
				<List title="Excessive funding pressures or funding control struggles">
					<ListItem>Short-term funding cycles disrupting long-term collaboration</ListItem>
					<ListItem>Power imbalances when funders dictate terms without community input</ListItem>
				</List>
				<ReferenceLink theme="dry-sage" refs={[{ name: 'Bustos et al. (2024)', link: '' }]} />
			</ListBlock>
		</div>
	</section>

	<StickyTitle>Network Processes</StickyTitle>

	<section class="container">
		<div class="grid grid-cols-2 gap-8">
			<ListBlock title="Facilitating Factors" theme="cornsilk">
				<List title="Exchanging information and knowledge">
					<ListItem theme="cornsilk">Sharing insights, data, and expertise across partners</ListItem
					>
					<ListItem theme="cornsilk">
						Promoting mutual learning and informed decision-making
					</ListItem>
					<ListItem theme="cornsilk">
						<strong>
							<Link
								theme="cornsilk"
								href="/competencies#Facilitating-Multidirectional-Knowledge-and-Skills-Exchange"
							>
								See: Competencies
							</Link>
						</strong>
					</ListItem>
				</List>
				<List title="Sharing resources">
					<ListItem theme="cornsilk">
						Ensuring equitable access to support collaboration goals
					</ListItem>
				</List>
				<List title="Effective and frequent communication">
					<ListItem theme="cornsilk"
						>Clearly defining roles, expectations, and priorities upfront</ListItem
					>
					<ListItem theme="cornsilk"
						>Maintaining transparency and alignment with shared mission</ListItem
					>
					<ListItem theme="cornsilk">Building trust through bidirectional dialogue</ListItem>
					<ListItem theme="cornsilk"
						>Supporting reconciliation-oriented partnership development</ListItem
					>
					<ListItem theme="cornsilk">
						<strong>
							<Link theme="cornsilk" href="/best-practices#communication">See: Best Practices</Link>
						</strong>
					</ListItem>
				</List>
				<List title="Informal relationship created">
					<ListItem theme="cornsilk">
						Developing personal rapport and shared understanding beyond formal agreements
					</ListItem>
				</List>
				<ReferenceLink theme="cornsilk" refs={[{ name: 'Bustos et al. (2024)', link: '' }]} />
			</ListBlock>
			<ListBlock title="Hindering Factors" theme="dry-sage">
				<List title="Poor communication between partners">
					<ListItem>Create a Road Map to align goals and timelines.</ListItem>
					<ListItem>
						<strong>
							<Link theme="dry-sage" href="/best-practices#communication">See: Best Practices</Link>
						</strong>
					</ListItem>
				</List>
				<List title="Lack of a common knowledge or shared terms between partners">
					<ListItem>Risk of misrepresentation or inaccurate portrayal of community needs</ListItem>
					<ListItem>
						Highlights oppressive structures in academic language; calls for intentional, inclusive
						dialogue to reduce barriers
					</ListItem>
				</List>
				<ReferenceLink theme="dry-sage" refs={[{ name: 'Bustos et al. (2024)', link: '' }]} />
			</ListBlock>
		</div>
	</section>
</div>
