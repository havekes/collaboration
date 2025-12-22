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
	type AccordionData = {
		title: string;
		theme: 'cornsilk' | 'dry-sage';
		leftContent: Content;
		rightContent: Content;
	};

	const accordionData: AccordionData[] = [
		{
			title: 'Start Early',
			theme: 'cornsilk',
			leftContent: [
				'Involve partners from the outset of project discussions.',
				'Integrate diverse stakeholders during initial planning stages.',
				'Use a buddy system to build strong personal connections and foster unity.'
			],
			rightContent: [
				'Facilitates strong personal connection.',
				'Ensures inclusivity, ethical consideration, and cultural relevance.'
			]
		},
		{
			title: 'Foster Team-Wide Collaboration',
			theme: 'dry-sage',
			leftContent: [
				'Promote constant communication: keep all partners informed and engaged.',
				'Encourage active dialogue and deliberation, emphasizing active listening, respectful questioning, and collaborative learning (“talking with,” not “talking at”) (Walker & Daniels, 2019).'
			],
			rightContent: [
				'Enhances creativity, problem-solving, and research quality.',
				'Builds trust and shared ownership.',
				'Facilitates unified goals and sustained engagement.',
				'Increases participant enrollment and broadens community impact.',
				'Strengthens team cohesion.'
			]
		},
		{
			title: 'Establish clear expectations & common understanding',
			theme: 'cornsilk',
			leftContent: [
				'Set clear expectations for roles, responsibilities, communication norms, and time commitments.',
				'Foster openness to accommodations and adaptations as needed.',
				'Use systems tools (e.g., “situation maps,” “generations walls”) to visualize challenges and future scenarios (Walker & Daniels, 2019, p. 3).',
				'Engage in shared imagination of best and worst possible futures to align perspectives (Walker & Daniels, 2019, p. 3).',
				'Ensure all parties understand project goals and their contributions (Farrell et al., 2024, p. 6964).'
			],
			rightContent: [
				'Creates a foundation for purposeful, goal-directed collaboration.',
				'Reduces misunderstandings and role ambiguity.',
				'Enhances coordination and accountability across partners.'
			]
		},
		{
			title: 'Enhance Communication',
			theme: 'dry-sage',
			leftContent: [
				'Designate a clear point of contact for streamlined communication.',
				{
					'Be transparent about': [
						'Project timelines and workload.',
						'Expected feedback types and frequency(Farrell et al., 2024).',
						'Desired outcomes and time commitments.',
						'Number and format of meetings, webinars, calls, and document reviews (Newcomb et al., 2021, p. 136).'
					]
				},
				'Maintain regular touchpoints to address questions promptly and offer task-specific training (Farrell et al., 2024, p. 6964).',
				'Invite honest feedback and constructive criticism.',
				'Identify key communicators or “translators” skilled in cross-boundary communication (Newcomb et al., 2021).',
				'Provide communication coaching and training (Walker & Daniels, 2019).',
				'Offer training using didactic and interactive methods (e.g., role-play with feedback, workshops, group discussions) (Tan et al., 2021).',
				'Incorporate reflective practices and feedback mechanisms (Tan et al., 2021).',
				'Develop a compelling rationale for engagement:  communicate purpose (Newcomb et al., 2021).',
				{
					'Sustain communication between meetings': [
						'Share pre-meeting materials to spark interest without overwhelming.',
						'Follow up post-meeting on action items.',
						'Ensure communication is concise, timely, and mutually agreed upon(Newcomb et al., 2021, p. 136).',
						'Choose appropriate communication modes (e.g., face-to-face, email).',
						'Assess partners’ preferences for information access, communication styles, and learning methods.'
					]
				}
			],
			rightContent: [
				'Ensures smooth communication, trust, and transparency.',
				'Promotes knowledge sharing and inclusion of diverse perspectives.',
				'Brings real-world relevance to research.',
				'Empowers participants and deepens understanding of research gaps.',
				'Advances knowledge and improves policy relevance through reciprocal learning (Newcomb et al., 2021, p. 136).'
			]
		},
		{
			title: 'Demonstrate Impact & Follow Through',
			theme: 'cornsilk',
			leftContent: [
				'Report the impact of partner contributions clearly.',
				'Show how partner insights have been integrated and how they shaped outcomes.',
				'Follow up on stakeholder participation (Walker & Daniels, 2019).',
				'Honor commitments made during the collaboration process (Walker & Daniels, 2019).'
			],
			rightContent: [
				'Builds trust and community support.',
				'Enhances transparency and shared ownership.',
				'Validates partners’ contributions and reinforces their value.'
			]
		},
		{
			title: 'Ensure Adequate Resources',
			theme: 'dry-sage',
			leftContent: [
				'Allocate sufficient time, funding, and personnel.',
				{
					Provide: [
						'Task-specific training.',
						'Mentorship programs.',
						'Research training materials.',
						'Workshops or online courses.',
						'EDI (Equity, Diversity, Inclusion) training for researchers.',
						'Implement clear compensation practices for partner contributions.'
					]
				}
			],
			rightContent: [
				'Supports capacity building for all collaborators.',
				'Fosters a more inclusive, equitable, and sustainable working environment.'
			]
		},
		{
			title: 'Promote Equitable Decision-Making',
			theme: 'cornsilk',
			leftContent: [
				'Address power imbalances by giving partners a governing voice.',
				'Clearly define partners’ roles in decision-making(Walker & Daniels, 2019).',
				'Clarify how partner input influences final decisions (Walker & Daniels, 2019).',
				'Define the “decision space”: identify which issues are open for co-determination.'
			],
			rightContent: [
				'Promotes fairness and shared leadership.',
				'Increases legitimacy and buy-in from all stakeholders.',
				'Strengthens democratic and ethical research practices.'
			]
		},
		{
			title: 'Ensure Flexibility',
			theme: 'dry-sage',
			leftContent: [
				'Accommodate flexible meeting times and formats.',
				{
					'Allow for iterative shifts in project direction (without full rescoping) (Newcomb et al., 2021, p. 136)':
						['Establish a process to discuss changes with funders (Newcomb et al., 2021, p. 136).']
				},
				'Develop contingency plans and anticipate potential surprises.'
			],
			rightContent: [
				'Enhances adaptability to emerging challenges.',
				'Supports responsiveness to real-time feedback and contextual changes.',
				'Maintains project relevance and feasibility.'
			]
		},
		{
			title: 'Determine a Clear Endpoint',
			theme: 'cornsilk',
			leftContent: [
				'Establish a logical, achievable endpoint that defines success (Newcomb et al., 2021, p. 137).',
				'Set measurable milestones to track progress (Newcomb et al., 2021, p. 137).',
				'Use milestones to assess success and guide shifts in priorities (Newcomb et al., 2021, p. 137).'
			],
			rightContent: [
				'Provides clarity on project closure.',
				'Enables evaluation of outcomes and impact.',
				'Supports reflection and knowledge transfer for future initiatives.'
			]
		}
	];
</script>

<svelte:head>
	<title>Best Practices - Collaboration</title>
</svelte:head>

<div class="my-12 flex flex-col items-center space-y-12">
	<!-- <section class="container px-8">
		<div class="space-y-6">
			<h1 class="text-4xl font-bold text-gray-800 text-shadow-cornsilk-200 text-shadow-xs">
				Best Practices for Effective Collaboration
			</h1>
			<p class="text-lg text-gray-700">
				Proven strategies to foster effective teamwork and achieve outstanding results together.
				(EXAMPLE)
			</p>
		</div>
	</section> -->

	<section class="container space-y-4">
		{#each accordionData as item, index}
			<AccordionItem
				title={item.title}
				theme={item.theme}
				open={openSections.includes(index)}
				onToggle={() => toggleSection(index)}
				leftContent={item.leftContent}
				rightContent={item.rightContent}
			/>
		{/each}
	</section>
</div>
