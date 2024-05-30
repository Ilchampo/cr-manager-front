<script lang="ts">
	import { goto } from '$app/navigation';

	import Icon from '$lib/components/Icon.svelte';
	import OnBoarding from '$lib/components/OnBoarding.svelte';
</script>

<OnBoarding
	stepNumber={1}
	stepTitle="Type of user"
	stepSubtitle="Please choose the type of user that represents you the most"
	disabledBackButton={true}
	disabledNextButton={false}
	handleBackButton={() => undefined}
	handleNextButton={() => goto('/onboarding/join')}
>
	<div class="flex flex-wrap items-center justify-center gap-8">
		<div class="flex flex-col md:flex-row w-full h-full p-4">
			<div class="flex flex-col gap-4 w-full md:w-[35%]">
				<header>
					<h4 class="h4">Which user type should I choose?</h4>
				</header>
				<article>
					<p class="font-light text-base">
						Choosing the correct user type is essential in order to be able to
						use the expected features. Here's a guide on how to choose the
						correct user type:
					</p>
					<ul class="list font-extralight text-base text-surface-900 p-4">
						<li>
							<span>
								<span class="mr-2"
									><Icon
										name="laptop"
										width="w-4"
										height="h-4"
										fill="fill-primary-500"
										ma
									/></span
								>Choose
								<b>Developer</b> if you expect to do code reviews.</span
							>
						</li>
						<li>
							<span>
								<span class="mr-2"
									><Icon
										name="people-group"
										width="w-4"
										height="h-4"
										fill="fill-primary-500"
										ma
									/></span
								>Choose <b>Manager</b> if you expect to manage releases and pull
								requests.</span
							>
						</li>
					</ul>
				</article>
			</div>
			<hr class="md:divider-vertical !border-r-2 h-full" />
			<div
				class="flex flex-col lg:flex-row w-full md:w-[60%] gap-4 justify-center items-center"
			>
				<div class="flex flex-col items-center justify-center w-full">
					<button
						class="card card-hover w-full md:w-auto flex flex-col p-4 justify-center items-center variant-ghost-surface"
					>
						<Icon
							name="laptop"
							width="w-40 lg:w-[80%]"
							height="h-40 lg:h-[80%]"
							fill="fill-surface-900"
						/>
						<span class="uppercase tracking-wide font-medium">Developer</span>
					</button>
				</div>
				<div class="flex flex-col items-center justify-center w-full">
					<button
						class="card card-hover w-full md:w-auto flex flex-col p-4 justify-center items-center variant-ghost-surface"
					>
						<Icon
							name="people-group"
							width="w-40 lg:w-[80%]"
							height="h-40 lg:h-[80%]"
							fill="fill-surface-900"
						/>
						<span class="uppercase tracking-wide font-medium">Manager</span>
					</button>
				</div>
			</div>
		</div>
	</div>
</OnBoarding>
