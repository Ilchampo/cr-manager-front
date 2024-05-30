<script lang="ts">
	import Icon from '$lib/components/Icon.svelte';
	import images from '$lib/assets/images';
	let showPassword = false;

	const handleShowPassword = (): void => {
		showPassword = !showPassword;
	};
</script>

<div class="card flex flex-col shadow-xl p-4 gap-4 max-w-[80%]">
	<header>
		<h3 class="h3">Sign up to CR Manager</h3>
		<span class="text-light">Enter your details below</span>
	</header>

	<button class="btn variant-ringed w-full" disabled>
		<img src={images.ICON_GOOGLE} alt="Google" width="16px" height="16px" />
		<span>Sign up with Google</span>
	</button>

	<div class="flex items-center justify-center gap-2">
		<hr class="!border-t-2 w-32" />
		<span class="text-center">Or sign up with</span>
		<hr class="!border-t-2 w-32" />
	</div>

	<form action="" method="post" class="flex flex-col gap-6">
		<div class="flex gap-6">
			<label class="label">
				<input class="input" type="text" placeholder="Firstname" />
			</label>
			<label class="label">
				<input class="input" type="text" placeholder="Lastname" />
			</label>
		</div>
		<label class="label">
			<input class="input" type="email" placeholder="Email" />
		</label>
		<label class="label">
			<div class="input-group input-group-divider grid-cols-[1fr_auto]">
				<input
					class="input"
					type={showPassword ? 'text' : 'password'}
					placeholder="Password"
				/>
				<div>
					<button type="button" on:click={handleShowPassword}>
						<Icon
							name={showPassword ? 'eye-slash' : 'eye'}
							fill="fill-surface-900"
						/>
					</button>
				</div>
			</div>
		</label>
		<label class="label">
			<input class="input" type="password" placeholder="Confirm Password" />
		</label>
		<button class="btn variant-filled-primary w-full mt-2">Sign up</button>
	</form>

	<div
		class="flex flex-col md:flex-row items-center justify-between font-light text-xs"
	>
		<span
			>Already have an account? <a href="/auth" class="text-tertiary-800"
				>Sign in</a
			></span
		>
		<span
			><a href="/auth/forgot" class="text-tertiary-800">Forgot password?</a
			></span
		>
	</div>
</div>
