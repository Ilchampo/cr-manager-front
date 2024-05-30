<script lang="ts">
	import { goto } from '$app/navigation';
</script>

<div class="card flex flex-col shadow-xl p-4 gap-4 max-w-[80%]">
	<header>
		<h3 class="h3">Forgot your password?</h3>
		<span class="text-light"
			>Enter the email address associated with your account, and we'll send you
			a link to reset your password.</span
		>
	</header>

	<form action="" method="post" class="flex flex-col">
		<label class="label">
			<input class="input" type="email" placeholder="Email" />
		</label>
		<button class="btn variant-filled-primary w-full mt-2"
			>Recover Password</button
		>
	</form>

	<button class="btn variant-ringed w-full" on:click={() => goto('/auth')}
		>Go Back</button
	>
</div>
