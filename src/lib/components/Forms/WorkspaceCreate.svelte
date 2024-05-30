<script lang="ts">
	import Icon from '$lib/components/Icon.svelte';
</script>

<div class="flex flex-col md:flex-row w-full h-full p-4">
	<div class="flex flex-col gap-4 w-full md:w-[35%]">
		<header>
			<h4 class="h4">How to create a Workspace?</h4>
		</header>
		<article class="">
			<p class="font-light text-base">
				Your workspace is where you are going to create new releases and manage
				them. Make sure to name it approperly to help Developers identify it
				easier!
			</p>
			<ul class="list font-extralight text-sm text-surface-900 p-4">
				<li>
					<Icon
						name="circle-check"
						width="w-4"
						height="h-4"
						fill="fill-success-500"
					/>
					<span>Add your project repository link.</span>
				</li>
				<li>
					<Icon
						name="circle-check"
						width="w-4"
						height="h-4"
						fill="fill-success-500"
					/>
					<span>Add your workspace name.</span>
				</li>
				<li>
					<Icon
						name="circle-check"
						width="w-4"
						height="h-4"
						fill="fill-surface-500"
					/>
					<span>Add your workspace logo.</span>
				</li>
				<li>
					<Icon
						name="circle-check"
						width="w-4"
						height="h-4"
						fill="fill-surface-500"
					/>
					<span>Add your workspace description.</span>
				</li>
			</ul>
		</article>
	</div>
	<hr class="md:divider-vertical !border-r-2 h-full" />
	<div class="flex w-full md:w-[60%]">
		<form action="" method="post" class="flex flex-col gap-2 w-full">
			<label class="label">
				<input class="input" type="text" placeholder="Project Repository" />
			</label>
			<label class="label">
				<input class="input" type="text" placeholder="Workspace Name" />
			</label>
			<label class="label">
				<input class="input" type="file" />
			</label>
			<label class="label">
				<textarea
					class="textarea"
					rows="4"
					placeholder="Workspace Description"
				/>
			</label>
		</form>
	</div>
</div>
