<script lang="ts">
	import picture1 from '$lib/assets/images/Picture1.png';
	import HighlightLink from '$lib/components/HighlightLink.svelte';
</script>

<div class="mx-auto my-6 max-w-6xl">
	<section>
		<div class="flex flex-row items-center gap-8 text-left">
			<div class="flex h-full w-2/3 items-center justify-center">
				<img
					src={picture1}
					alt="Key factors to the success of partnerships"
					class="h-auto w-full rounded-xl"
				/>
			</div>
			<div class="flex-1 space-y-4">
				<h2 class="text-left text-2xl leading-tight font-bold text-gray-800">
					Key factors to the success of partnerships
				</h2>
				<div class="space-y-2 rounded-2xl bg-dry-sage-50 p-4">
					<h3 class="text-left font-bold">
						<div class="flex items-center gap-3">
							<div
								class="flex h-10 w-10 shrink-0 items-center justify-center rounded-full bg-dry-sage-200"
							>
								<svg
									xmlns="http://www.w3.org/2000/svg"
									viewBox="0 0 512 512"
									class="h-5 w-5 fill-dry-sage-800"
								>
									<!--!Font Awesome Free v7.1.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2025 Fonticons, Inc.-->
									<path
										d="M416 208c0 45.9-14.9 88.3-40 122.7L502.6 457.4c12.5 12.5 12.5 32.8 0 45.3s-32.8 12.5-45.3 0L330.7 376C296.3 401.1 253.9 416 208 416 93.1 416 0 322.9 0 208S93.1 0 208 0 416 93.1 416 208zM208 352a144 144 0 1 0 0-288 144 144 0 1 0 0 288z"
									></path>
								</svg>
							</div>
							<span>Want to improve your partnership?</span>
						</div>
					</h3>
					<p class="text-left text-base leading-relaxed text-gray-800">
						See what factors help or hinder collaboration and the success of your partnerships.
					</p>
				</div>
				<HighlightLink href="#" text="View facilitators and hindering factors" />
			</div>
		</div>
	</section>
</div>
