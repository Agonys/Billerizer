<script lang="ts">
	import "../app.postcss";
	import Sidebar from "$lib/components/Sidebar/Sidebar.svelte";

	// Floating UI for Popups
	import { computePosition, autoUpdate, flip, shift, offset, arrow } from "@floating-ui/dom";
	import { AppShell, storePopup } from "@skeletonlabs/skeleton";
	import Appbar from "$lib/components/Appbar/Appbar.svelte";
	storePopup.set({ computePosition, autoUpdate, flip, shift, offset, arrow });
</script>

<AppShell>
	<svelte:fragment slot="header">
		<Appbar />
	</svelte:fragment>
	<svelte:fragment slot="sidebarLeft">
		<Sidebar />
	</svelte:fragment>

	<slot />
</AppShell>
