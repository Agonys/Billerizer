<script lang="ts">
	import type { INavItemsLinks, INavItemsRegular } from "$lib/types";
	import SidebarItem from "./SidebarItem.svelte";

	export let sectionTitle: string | undefined = undefined;
	export let navItems: (INavItemsRegular | INavItemsLinks)[] = [];
</script>

<div class="flex flex-col gap-2">
	{#if sectionTitle}
		<h6 class="h6 text-gray-500 text-xs">{sectionTitle}</h6>
	{/if}
	<ul class="flex flex-col gap-1">
		{#each navItems as navItem}
			{#if "href" in navItem}
				<SidebarItem {navItem} />
			{:else}
				<SidebarItem {navItem} />
			{/if}
		{/each}
	</ul>
</div>
