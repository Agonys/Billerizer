<script lang="ts">
	import { AppBar, Avatar } from "@skeletonlabs/skeleton";
	import { BookCopy } from "lucide-svelte";
</script>

<AppBar shadow="shadow-xl" background="bg-gray-800" border="border-b border-gray-700">
	<svelte:fragment slot="lead">
		<div class="flex gap-4">
			<BookCopy size={40} class="text-secondary-500" />
			<h2 class="h2">Billerizer</h2>
		</div>
	</svelte:fragment>
	<svelte:fragment slot="trail">
		<div class="flex gap-4">
			<div class="flex flex-col items-end">
				<p>Agonys</p>
				<span class="text-gray-500">SampleMail@gmail.com</span>
			</div>
			<Avatar
				background="bg-surface-900"
				initials="Agonys"
				src="https://i.imgur.com/VY7MAUr.png"
				width="w-12"
			/>
		</div>
	</svelte:fragment>
</AppBar>
