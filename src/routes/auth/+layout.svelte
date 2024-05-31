<script lang="ts">
	import Icon from '$lib/components/Icon.svelte';
	import images from '$lib/assets/images';
</script>

<div class="grid grid-cols-1 md:grid-cols-2 h-screen w-screen">
	<div
		class="hidden md:flex flex-col h-full bg-gradient-to-br from-tertiary-900 to-tertiary-500"
	>
		<div class="flex flex-col h-full justify-between p-16">
			<img src={images.DEMO_USERS} alt="Demo Users" />

			<ul class="flex flex-col gap-4">
				<li class="flex items-center justify-start gap-4">
					<Icon
						name="circle-check"
						width="w-6"
						height="h-6"
						fill="fill-primary-100"
					/>
					<span class="font-medium text-xl text-primary-100">
						Create or join a workspace to manage all your project releases.
					</span>
				</li>
				<li class="flex items-center justify-start gap-4">
					<Icon
						name="circle-check"
						width="w-6"
						height="h-6"
						fill="fill-primary-100"
					/>
					<span class="font-medium text-xl text-primary-100">
						Keep track of all your code reviews status.
					</span>
				</li>
				<li class="flex items-center justify-start gap-4">
					<Icon
						name="circle-check"
						width="w-6"
						height="h-6"
						fill="fill-primary-100"
					/>
					<span class="font-medium text-xl text-primary-100">
						Get notifications about your release or pull request status.
					</span>
				</li>
			</ul>
		</div>
	</div>
	<div class="flex flex-col h-full items-center justify-center">
		<slot />
	</div>
</div>
