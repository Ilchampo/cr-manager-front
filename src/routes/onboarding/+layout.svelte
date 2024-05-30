<div class="diagonal-split-bg bg-white">
	<div
		class="flex flex-col items-center justify-center h-screen w-screen relative z-10"
	>
		<slot />
	</div>
</div>

<style>
	.diagonal-split-bg {
		@apply bg-gradient-to-br from-primary-900 to-primary-500 relative w-screen h-screen;
	}
	.diagonal-split-bg::before {
		content: '';
		clip-path: polygon(0 100%, 100% 0, 100% 100%, 0 100%);
		@apply z-0 w-full h-full top-0 left-0 absolute bg-surface-100;
	}
</style>
