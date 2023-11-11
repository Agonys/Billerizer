<script lang="ts">
	import { Home, FileStack, Folder, FileClock, FilePlus, FolderPlus } from "lucide-svelte";
	import SidebarList from "./SidebarList.svelte";
	import type { INavItemsLinks } from "$lib/types";

	const navItems: INavItemsLinks[] = [
		{
			name: "Dashboard",
			icon: Home,
			href: "/"
		},
		{
			name: "Bills history",
			icon: FileStack,
			href: "/history"
		},
		{
			name: "Categories",
			icon: Folder,
			href: "/categories"
		},
		{
			name: "Logs",
			icon: FileClock,
			href: "/logs"
		}
	];
</script>

<div class="flex flex-col p-4 bg-gray-800 w-[250px] h-full justify-between">
	<SidebarList sectionTitle="Navigation" {navItems} />
	<div class="flex flex-col gap-2 w-full">
		<button type="button" class="btn variant-filled-secondary">
			<span><FilePlus /></span>
			<span>Add bill</span>
		</button>
		<button type="button" class="btn variant-outline-secondary">
			<span><FolderPlus /></span>
			<span>Add category</span>
		</button>
	</div>
</div>
