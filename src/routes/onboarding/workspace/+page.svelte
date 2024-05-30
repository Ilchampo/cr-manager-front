<script lang="ts">
	import OnBoarding from '$lib/components/OnBoarding.svelte';
	import WorkspaceCreate from '$lib/components/Forms/WorkspaceCreate.svelte';
	import { goto } from '$app/navigation';
</script>

<OnBoarding
	stepNumber={2}
	stepTitle="Create a workspace"
	stepSubtitle="Please complete the following information to create a workspace and ask Developers to join"
	disabledBackButton={false}
	disabledNextButton={false}
	handleBackButton={() => goto('/onboarding')}
	handleNextButton={() => goto('/onboarding/loading')}
>
	<div class="flex flex-wrap items-center justify-center gap-8">
		<WorkspaceCreate />
	</div>
</OnBoarding>
