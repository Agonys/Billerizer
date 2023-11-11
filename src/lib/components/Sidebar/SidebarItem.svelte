<script lang="ts">
	import type { INavItemsLinks, INavItemsRegular } from "$lib/types";
	import { page } from "$app/stores";

	const currentRoute = $page.route.id;

	export let navItem: INavItemsLinks | INavItemsRegular;
</script>

{#if "href" in navItem}
	<li>
		<a
			class={`transition ease-linear flex gap-2 font-medium hover:bg-gray-900 p-2 rounded-lg ${
				currentRoute === navItem.href
					? "text-secondary-500 bg-gray-900"
					: "text-gray-500 hover:text-white"
			}`}
			href={navItem.href}><svelte:component this={navItem.icon} /> {navItem.name}</a
		>
	</li>
{:else}
	<li
		class="flex gap-2 font-medium hover:bg-sufrace-900 text-gray-500 hover:text-white p-2 rounded-lg"
		on:keypress={navItem.onClick}
		on:click={navItem.onClick}
		role="presentation"
	>
		<svelte:component this={navItem.icon} />
		{navItem.name}
	</li>
{/if}
