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
		id?: string;
		theme: 'cornsilk' | 'dry-sage';
		leftContent: Content;
		rightContent: Content;
		refs: Array<Ref>;
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
			],
			refs: [
				{
					name: 'Farrell et al. (2024)',
					link: ''
				}
			]
		},
		{
			title: 'Foster Team-Wide Collaboration',
			theme: 'dry-sage',
			leftContent: [
				'Promote constant communication: keep all partners informed and engaged.',
				'Encourage active dialogue and deliberation, emphasizing active listening, respectful questioning, and collaborative learning.'
			],
			rightContent: [
				'Enhances creativity, problem-solving, and research quality.',
				'Builds trust and shared ownership.',
				'Facilitates unified goals and sustained engagement.',
				'Increases participant enrollment and broadens community impact.',
				'Strengthens team cohesion and mutual accountability.'
			],
			refs: [
				{
					name: 'Farrell et al. (2024)',
					link: ''
				},
				{
					name: 'Walker & Daniels (2019)',
					link: ''
				}
			]
		},
		{
			title: 'Establish Clear Expectations & Common Understanding',
			theme: 'cornsilk',
			leftContent: [
				'Set clear expectations for roles, responsibilities, communication norms, and time commitments.',
				'Foster openness to accommodations and adaptations as needed.',
				'Use systems tools (e.g., “situation maps,” “generations walls”) to visualize challenges and future scenarios.',
				'Engage in shared imagination of best and worst possible futures to align perspectives.',
				'Ensure all parties understand project goals and their contributions.'
			],
			rightContent: [
				'Creates a foundation for purposeful, goal-directed collaboration.',
				'Reduces misunderstandings and role ambiguity.',
				'Enhances coordination and accountability across partners.'
			],
			refs: [
				{
					name: 'Farrell et al. (2024)',
					link: ''
				},
				{
					name: 'Walker & Daniels (2019)',
					link: ''
				}
			]
		},
		{
			title: 'Enhance Communication',
			id: 'communication',
			theme: 'dry-sage',
			leftContent: [
				'Designate a clear point of contact for streamlined communication.',
				{
					'Be transparent about': [
						'Project timelines and workload.',
						'Expected feedback types and frequency.',
						'Desired outcomes and time commitments.',
						'Number and format of meetings, webinars, calls, and document reviews.'
					]
				},
				'Maintain regular touchpoints to address questions promptly and offer task-specific training.',
				{
					'Sustain communication between meetings': [
						'Share pre-meeting materials to spark interest without overwhelming.',
						'Follow up post-meeting on action items.',
						'Ensure communication is concise, timely, and mutually agreed upon.',
						'Choose appropriate communication modes (e.g., face-to-face, email, social media).',
						'Assess partners’ preferences for information access, communication styles, and learning methods.'
					]
				},
				'Invite honest feedback and constructive criticism.',
				'Identify key communicators or “translators” skilled in cross-boundary communication.',
				'Provide communication coaching and training.',
				'Offer training using didactic and interactive methods (e.g., role-play with feedback, workshops, group discussions).',
				'Incorporate reflective practices and feedback mechanisms.',
				'Develop a compelling rationale for engagement:  communicate purpose.'
			],
			rightContent: [
				'Ensures smooth communication, trust, and transparency.',
				'Promotes knowledge sharing and inclusion of diverse perspectives.',
				'Brings real-world relevance to research.',
				'Empowers participants and deepens understanding of research gaps.',
				'Advances knowledge and improves policy relevance through reciprocal learning.'
			],
			refs: [
				{
					name: 'Farrell et al. (2024)',
					link: ''
				},
				{
					name: 'Newcomb et al. (2021)',
					link: ''
				},
				{
					name: 'Tan et al. (2021)',
					link: ''
				},
				{
					name: 'Walker & Daniels (2019)',
					link: ''
				}
			]
		},
		{
			title: 'Demonstrate Impact & Follow Through',
			theme: 'cornsilk',
			leftContent: [
				'Report the impact of partner contributions clearly.',
				'Show how partner insights have been integrated and how they shaped outcomes.',
				'Follow up on stakeholder participation.',
				'Honor commitments made during the collaboration process.'
			],
			rightContent: [
				'Builds trust and community support.',
				'Enhances transparency and shared ownership.',
				'Validates partners’ contributions and reinforces their value.'
			],
			refs: [
				{
					name: 'Farrell et al. (2024)',
					link: ''
				},
				{
					name: 'Walker & Daniels (2019)',
					link: ''
				}
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
			],
			refs: [
				{
					name: 'Farrell et al. (2024)',
					link: ''
				}
			]
		},
		{
			title: 'Promote Equitable Decision-Making',
			theme: 'cornsilk',
			leftContent: [
				'Address power imbalances by giving partners a governing voice.',
				'Clearly define partners’ roles in decision-making.',
				'Clarify how partner input influences final decisions.',
				'Define the “decision space”: identify which issues are open for co-determination.'
			],
			rightContent: [
				'Promotes fairness and shared leadership.',
				'Increases legitimacy and buy-in from all stakeholders.',
				'Strengthens democratic and ethical research practices.'
			],
			refs: [
				{
					name: 'Farrell et al. (2024)',
					link: ''
				},
				{
					name: 'Walker & Daniels (2019)',
					link: ''
				}
			]
		},
		{
			title: 'Ensure Flexibility',
			theme: 'dry-sage',
			leftContent: [
				'Accommodate flexible meeting times and formats.',
				{
					'Allow for iterative shifts in project direction (without full rescoping)': [
						'Establish a process to discuss changes with funders.'
					]
				},
				'Develop contingency plans and anticipate potential surprises.'
			],
			rightContent: [
				'Enhances adaptability to emerging challenges.',
				'Supports responsiveness to real-time feedback and contextual changes.',
				'Maintains project relevance and feasibility.'
			],
			refs: [
				{
					name: 'Farrell et al. (2024)',
					link: ''
				},
				{
					name: 'Newcomb et al. (2021)',
					link: ''
				}
			]
		},
		{
			title: 'Determine a Clear Endpoint',
			theme: 'cornsilk',
			leftContent: [
				'Establish a logical, achievable endpoint that defines success.',
				'Set measurable milestones to track progress.',
				'Use milestones to assess success and guide shifts in priorities.'
			],
			rightContent: [
				'Provides clarity on project closure.',
				'Enables evaluation of outcomes and impact.',
				'Supports reflection and knowledge transfer for future initiatives.'
			],
			refs: [
				{
					name: 'Newcomb et al. (2021)',
					link: ''
				}
			]
		}
	];
</script>

<svelte:head>
	<title>Best Practices</title>
</svelte:head>

<div class="my-8 flex flex-col items-center space-y-8">
	<section class="container">
		<h1 class="text-3xl font-bold text-light-bronze-800">
			Best Practices for Effective Collaboration
		</h1>
	</section>

	<section class="container space-y-4">
		{#each accordionData as item, index}
			<AccordionItem
				title={item.title}
				id={item.id}
				theme={item.theme}
				open={openSections.includes(index)}
				onToggle={() => toggleSection(index)}
				leftTitle="How to foster it?"
				leftContent={item.leftContent}
				rightTitle="Why do it?"
				rightContent={item.rightContent}
				refs={item.refs}
			/>
		{/each}
	</section>
</div>
