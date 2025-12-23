<script lang="ts">
	import AccordionItem from '$lib/components/AccordionItem.svelte';

	let openSections = [0]; // First section open by default

	let toggleSection = (index: number) => {
		if (openSections.includes(index)) {
			openSections = openSections.filter((i) => i !== index);
		} else {
			openSections = [...openSections, index];
		}
	};

	type Content = Array<string | Record<string, Array<string>>>;
	type Ref = {
		name: string;
		link: string;
	};
	type AccordionData = {
		title: string;
		theme: 'cornsilk' | 'dry-sage';
		leftContent: Content;
		middleContent: Content;
		rightContent: Content;
		refs: Array<Ref>;
		refsAlt?: Array<Ref>;
	};

	const accordionData: AccordionData[] = [
		{
			title: 'Reflexivity on Identity and Power',
			theme: 'cornsilk',
			leftContent: [
				{
					'This competency involves recognizing how personal and social identities (shaped by intersectional factors such as gender, age, race, class, disability, religion, caste, language, education, and geography) influence how individuals and groups perceive, relate to, and interact with one another in research partnerships. It includes':
						[
							'Understanding how social location shapes experiences of power, privilege, and marginalization.',
							'Being reflexive on how external researchers may be perceived by communities based on identity markers.',
							'Acknowledging historical and systemic inequities that contribute to distrust between academic institutions and communities, especially among marginalized groups.',
							'Being open to alternative ways of knowing, doing, and organizing, and understanding intragroup disparities.',
							'Critically reflecting on personal, locational, institutional, and structural power to actively redress imbalances in partnership dynamics.'
						]
				}
			],
			middleContent: [
				'Builds mutual respect and cultural humility.',
				'Reduces risk of reproducing inequities in research.',
				'Enhances trust and legitimacy of the partnership.',
				'Increases sensitivity to power dynamics and historical context.',
				'Promotes inclusive participation and shared ownership.',
				'Supports co-leadership and transparent communication.',
				'Leads to more socially cohesive and sustainable collaborations.'
			],
			rightContent: [
				'Conduct structured reflexivity sessions to explore identity, positionality, and power dynamics among partners. Explore questions such as “What relationships exist and how are they influencing the research and the people involved? What power dynamics are at play?” (Olmos-Vega et al., 2022, p. 244). Additional questions can be found in Olmos-Vega et al. (2022).',
				'Use narrative and visual tools such as the Tree of Life, River of Life, or metaphor-based reflection to explore identity in relation to others.',
				'Apply Person-Centred Approaches to build deeper community connections.',
				'Exploring both individual and collective identity using tools such as cultural mapping, strengths inventories, and life histories.',
				'Encourage partners to reflect on how their institutional affiliations shape their roles and perceptions.'
			],
			refs: [
				{
					name: 'Ozano et al. (2024)',
					link: ''
				}
			],
			refsAlt: [
				{
					name: 'Olmos-Vega et al. (2022)',
					link: ''
				}
			]
		},
		{
			title: 'Understanding Community Context to Work Synergistically',
			theme: 'dry-sage',
			leftContent: [
				'Understanding how communities function socially and structurally.',
				'Identifying, leveraging, and respecting community strengths and limitations.',
				'Mapping formal and informal governance systems (e.g., in informal settlements) that influence health and well-being.',
				'Assessing structural enablers and barriers (e.g., access to services, power hierarchies).',
				'Recognizing motivations and influence of gatekeepers who may amplify or suppress marginalized voices.',
				'Commitment to contextual awareness, including historical, cultural, and political realities affecting communities.'
			],
			middleContent: [
				'Development of more holistic and coordinated strategies through collective action.',
				'Strengthened inter-organizational and community networks that support long-term engagement.',
				'Broader access to shared resources, expertise, and infrastructure.',
				'Increased readiness for contextually grounded research or intervention.',
				'Greater potential for influencing local policy and service delivery.',
				'Deeper insights into community priorities and needs.',
				'Emergence of new, community-informed research questions.'
			],
			rightContent: [
				'Conduct asset-based community assessments to identify strengths, skills, and local resources.',
				'Use governance assessments (e.g., "Governance Diaries") to uncover formal and informal decision-making networks.',
				'Facilitate reflective sessions among partners to identify their contributions, potential biases, and organizational assets or limitations.',
				{
					'Undertake place-based assessments such as': [
						'GIS mapping of resources and risks.',
						'Structured walking tours to observe neighborhood conditions.',
						'Windshield surveys (systematic driving observations).',
						'Use of field checklists to document physical, social, and environmental assets or concerns.'
					]
				}
			],
			refs: [
				{
					name: 'Ozano et al. (2024)',
					link: ''
				}
			]
		},
		{
			title: 'Facilitating Multidirectional Knowledge and Skills Exchange',
			theme: 'cornsilk',
			leftContent: [
				{
					'This competency focuses on fostering environments where diverse forms of knowledge—(e.g. experiential, contextual, technical, political, relational, historical, and emotional) are recognized, valued, and exchanged equitably. It involves':
						[
							'Appreciating different knowledge systems and epistemologies.',
							'Identifying individual and collective capacities and skill gaps.',
							'Being open to learning from people with different lived experiences.',
							'Understanding social learning as a process of social-ecological change through peer-to-peer exchange.',
							'Tailoring knowledge mobilization methods to ensure accessibility, relevance, and inclusivity.',
							'Supporting all partners to reflect on what works (or doesn’t) in practice and how shared learning creates impact.'
						]
				},
				'Requires ongoing capacity needs assessments and co-developed capacity-strengthening plans.'
			],
			middleContent: [
				'Increases accessibility of research outputs.',
				'Strengthens mutual understanding across diverse partners.',
				'Supports transparency in discussing needs, limitations, and concerns.',
				'Builds individual and organizational capacity.'
			],
			rightContent: [
				'Co-develop a capacity-strengthening strategy that evolves over time',
				'Support community researchers to attend and present at academic and policy conferences',
				{
					Measures: [
						'Use evaluation methods such as ‘Most Significant Change’ exercise or Ripple Effect Mapping to capture learning and impact.'
					]
				}
			],
			refs: [
				{
					name: 'Ozano et al. (2024)',
					link: ''
				}
			]
		},
		{
			title: 'Co-Leadership Skills',
			theme: 'dry-sage',
			leftContent: [
				{
					'This competency involves continuously examining and adapting partnership governance to support democratic practices throughout the research process. It includes':
						[
							'Assessing compatibility of values, attitudes, and beliefs among partners (“goodness of fit”).',
							'Balancing competing interests among community members, academic researchers, and supporting organizations.',
							'Upholding shared values, ethical practices, and positive partnership behaviors.',
							'Demonstrating flexibility, openness, compromise, and commitment to collective progress.',
							'Recognizing structural enablers and barriers (e.g., policies, procurement systems, communication channels).',
							'Practicing democratic leadership and facilitation',
							'Understanding diverse roles within groups (e.g., catalyst, facilitator, co-learner, consultant).',
							'Ensuring shared decision-making, information flow, resource allocation, and leadership development.'
						]
				}
			],
			middleContent: [
				'Establishes a shared, trusted vision for the research.',
				'Increases inclusive and meaningful participation.',
				'Strengthens internal relationships and external community linkages.'
			],
			rightContent: [
				'Jointly develop operating procedures (e.g., ground rules, memoranda of understanding).',
				'Co-create a shared vision, mission, and measurable goals.',
				'Establish transparent communication mechanisms (e.g., shared agendas, meeting notes, communication logs).',
				'Develop and adopt a Code of Research Ethics.',
				'Provide leadership and facilitation training for all partners.',
				{
					Measures: [
						'Monitor decision-making equity using qualitative and quantitative indicators (e.g., representation in subgroups, leadership rotation, policy development).'
					]
				}
			],
			refs: [
				{
					name: 'Ozano et al. (2024)',
					link: ''
				}
			]
		},
		{
			title: 'Adaptive Learning Capacity',
			theme: 'cornsilk',
			leftContent: [
				{
					'CBPR is inherently cyclical and iterative. This competency involves the ongoing ability to assess':
						[
							'Community ecosystem readiness (motivations, capacities of stakeholders).',
							'Sociocultural, economic, and political contexts (e.g., elections, conflict, social movements).',
							'Partner readiness for action.',
							'Successes and challenges at each research stage to inform adaptation.'
						]
				},
				{
					'It includes': [
						'Assessing community “readiness” to act on a matter.',
						'Understanding community experiences with the problem and prior solutions.',
						'Listening to diverse perspectives, emotions, and lived experiences.',
						'Designing and testing ideas with rapid feedback loops.',
						'Reflecting on one’s own practice and stakeholder motivations.',
						'Monitoring ethical practice throughout the research process.'
					]
				}
			],
			middleContent: [
				'Leads to responsive, context-sensitive research.',
				'Supports continuous learning and adaptation.',
				'Strengthens capacity for future community-led research.',
				'Improves accuracy in identifying community priorities.',
				'Encourages systematic reflection on successes and limitations.',
				'Enhances researcher ability to respond to evolving community needs.'
			],
			rightContent: [
				'Engage in joint problem-solving to translate evidence into action through understandable format.',
				'Develop realistic action plans that identify gaps, root causes, and solutions.',
				'Modify strategies based on field notes and post-implementation assessments.',
				'Use learning cycles (act-reflect-revise) to iteratively improve plans.',
				'Co-analyze data in collaborative sessions to identify key challenges and priorities.',
				'Translate research data into accessible “discussion tools” (e.g., tables, infographics, one-liners).',
				'Use participatory methods to gather immediate feedback on interventions.'
			],
			refs: [
				{
					name: 'Ozano et al. (2024)',
					link: ''
				}
			]
		}
	];
</script>

<svelte:head>
	<title>Core Competencies for Equitable Partnership</title>
</svelte:head>

<div class="my-8 flex flex-col items-center space-y-8">
	<section class="container">
		<h1 class="text-3xl font-bold text-cornsilk-800">Core Competencies</h1>
	</section>

	<section class="container space-y-4">
		{#each accordionData as item, index}
			<AccordionItem
				title={item.title}
				theme={item.theme}
				open={openSections.includes(index)}
				onToggle={() => toggleSection(index)}
				leftTitle="What it involves"
				leftContent={item.leftContent}
				middleTitle="Why it matters"
				middleContent={item.middleContent}
				rightTitle="How to implement"
				rightContent={item.rightContent}
				refs={item.refs}
				refsAlt={item.refsAlt}
			/>
		{/each}
	</section>
</div>
