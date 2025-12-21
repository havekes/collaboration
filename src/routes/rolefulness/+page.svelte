<script>
	import Card from '$lib/components/Card.svelte';
	import { faArrowRightLong, faArrowsLeftRight } from '@fortawesome/free-solid-svg-icons';
	import { FontAwesomeIcon } from '@fortawesome/svelte-fontawesome';
</script>

<div class="my-12 flex flex-col items-center space-y-12">
	<section class="container px-8">
		<h1 class="text-4xl font-bold text-gray-800 text-shadow-cornsilk-200 text-shadow-xs">
			Rolefulness
		</h1>
	</section>

	<section class="container grid grid-cols-2">
		<div class="flex items-center">
			<Card theme="dry-sage" class="ml-50 w-70 rounded-full px-20 py-10 text-center">
				<h2 class="text-2xl font-bold text-dry-sage-900">Social</h2>
			</Card>
		</div>
		<div class="space-y-4 pr-60">
			<Card theme="dry-sage">My role is necessary for other people.</Card>
			<Card theme="dry-sage">I can apply my strong point for society.</Card>
			<Card theme="dry-sage">I have a role in the group I belong to.</Card>
			<Card theme="dry-sage">I am useful in society.</Card>
		</div>
		<div class="text-2xl text-dry-sage-700">
			<div class="absolute top-41 ml-135 -rotate-24 text-2xl">
				<FontAwesomeIcon icon={faArrowRightLong} />
			</div>
			<div class="absolute top-62 ml-135 -rotate-6">
				<FontAwesomeIcon icon={faArrowRightLong} />
			</div>
			<div class="absolute top-83 ml-135 rotate-6">
				<FontAwesomeIcon icon={faArrowRightLong} />
			</div>
			<div class="absolute top-104 ml-135 rotate-24">
				<FontAwesomeIcon icon={faArrowRightLong} />
			</div>
		</div>
	</section>

	<section class="container grid grid-cols-2">
		<div class="flex items-center">
			<Card theme="light-bronze" class="ml-50 w-70 rounded-full px-20 py-10 text-center">
				<h2 class="text-2xl font-bold text-light-bronze-900">Internal</h2>
			</Card>
		</div>
		<div class="space-y-4 pr-60">
			<Card theme="light-bronze">I realize my individuality by my role.</Card>
			<Card theme="light-bronze">I am satisfied with my role.</Card>
			<Card theme="light-bronze">I gain confidence because of my role.</Card>
		</div>
		<div class="text-2xl text-light-bronze-700">
			<div class="absolute top-139 ml-135 -rotate-18 text-2xl">
				<FontAwesomeIcon icon={faArrowRightLong} />
			</div>
			<div class="absolute top-160 ml-135">
				<FontAwesomeIcon icon={faArrowRightLong} />
			</div>
			<div class="absolute top-180 ml-135 rotate-18">
				<FontAwesomeIcon icon={faArrowRightLong} />
			</div>
		</div>
	</section>

	<div class="absolute top-120 mr-150 scale-125 rotate-90 text-2xl text-dry-sage-700">
		<FontAwesomeIcon icon={faArrowsLeftRight} />
	</div>
</div>
