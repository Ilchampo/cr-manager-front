<script lang="ts">
	import { goto } from '$app/navigation';
	import OnBoarding from '$lib/components/OnBoarding.svelte';
	import WorkspaceCode from '$lib/components/Forms/WorkspaceCode.svelte';
</script>

<OnBoarding
	stepNumber={2}
	stepTitle="Join Workspace"
	stepSubtitle="Please enter the Workspace code to join it"
	disabledBackButton={false}
	disabledNextButton={false}
	handleBackButton={() => goto('/onboarding')}
	handleNextButton={() => goto('/onboarding/loading')}
>
	<div class="flex flex-wrap items-center justify-center gap-8">
		<div class="flex flex-col md:flex-row w-full h-full p-4 gap-4">
			<div class="flex flex-col gap-4 w-full md:w-[35%]">
				<header>
					<h4 class="h4">How do I get a workspace code?</h4>
				</header>
				<article>
					<p class="font-light text-base">
						Your <b>Manager</b> should have received a workspace code once completed
						the On Boarding process.
					</p>
				</article>
			</div>
			<hr class="md:divider-vertical !border-r-2 h-full" />
			<div
				class="flex flex-col lg:flex-row w-full md:w-[60%] gap-4 justify-center items-center"
			>
				<WorkspaceCode />
			</div>
		</div>
	</div>
</OnBoarding>
