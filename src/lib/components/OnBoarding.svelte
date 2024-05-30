<script lang="ts">
	export let stepNumber: number;
	export let stepTitle: string;
	export let stepSubtitle: string;
	export let disabledBackButton: boolean;
	export let disabledNextButton: boolean;
	export let handleBackButton: () => void;
	export let handleNextButton: () => void;
</script>

<div
	class="card shadow-xl flex flex-col p-4 h-[95%] w-[95%] md:h-[60%] md:w-[60%] gap-4 justify-between"
>
	<div class="flex flex-col gap-4 w-full">
		<header class="flex gap-4 justify-start items-center">
			<div
				class="flex bg-gradient-to-br from-primary-900 to-primary-500 rounded-xl h-8 w-8 p-4 md:h-14 md:w-14 justify-center items-center"
			>
				<span class="text-2xl font-semibold text-primary-100">{stepNumber}</span
				>
			</div>
			<div class="flex flex-col justify-between">
				<h3 class="h3">On Boarding: {stepTitle}</h3>
				<span class="font-light">{stepSubtitle}</span>
			</div>
		</header>
		<hr class="!border-t-2" />
	</div>

	<div class="flex flex-col gap-4 overflow-scroll">
		<slot />
	</div>

	<div class="flex flex-col gap-4 w-full">
		<hr class="!border-t-2" />
		<div class="flex w-full justify-between items-center self-end">
			<button
				class="btn variant-filled-surface"
				on:click={handleBackButton}
				disabled={disabledBackButton}>Back</button
			>
			<button
				class="btn variant-filled-primary"
				on:click={handleNextButton}
				disabled={disabledNextButton}>Next</button
			>
		</div>
	</div>
</div>
