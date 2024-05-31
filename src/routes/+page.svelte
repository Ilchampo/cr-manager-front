<script lang="ts">
	import Bubbles from '$lib/components/Bubbles.svelte';
	import images from '$lib/assets/images';

	import { goto } from '$app/navigation';
</script>

<div
	class="flex flex-col w-screen h-screen bg-gradient-to-r from-primary-900 to-primary-500 relative"
>
	<div class="flex flex-col h-full w-full absolute">
		<div class="grid grid-cols-1 md:grid-cols-2 z-10 h-full">
			<div class="flex flex-col gap-8 justify-center items-start p-12 h-full">
				<h1
					class="h1 text-surface-100 font-semibold tracking-wide text-5xl md:text-7xl"
				>
					Planning project
					<span class="gradient-tertiary font-bold">releases</span> was never
					this
					<span class="gradient-tertiary font-bold">easy</span>.
				</h1>
				<div class="flex gap-4 justify-start items-center">
					<button
						class="btn variant-filled-primary justify-center items-center w-32"
						on:click={() => goto('/auth')}
					>
						Sign in
					</button>
					<button
						class="btn variant-filled-surface justify-center items-center w-32"
						on:click={() => goto('/auth/signup')}
					>
						Sign up
					</button>
				</div>
			</div>
			<div class="hidden md:flex flex-col h-full justify-center items-center">
				<img src={images.DEMO_USERS} alt="Demo users" />
			</div>
		</div>
	</div>
	<div class="flex flex-col h-full w-full relative opacity-50 z-0">
		<Bubbles />
	</div>
</div>
