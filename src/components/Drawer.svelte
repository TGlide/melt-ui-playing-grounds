<script lang="ts">
	import type { CreateDialogReturn } from '@melt-ui/svelte';
	import { fade, fly } from 'svelte/transition';

	// import DrawerContent from './DrawerContent.svelte';
	import DrawerHeader from './DrawerHeader.svelte';

	export let drawer: CreateDialogReturn;

	const { portal, overlay, content, open } = drawer;
</script>

<div use:portal>
	{#if $open}
		<div
			{...$overlay}
			class="fixed inset-0 z-20 bg-gray-800/50"
			transition:fade={{ duration: 150 }}
		/>
		<div
			{...$content}
			use:content
			class="fixed right-0 top-0 z-50 h-screen w-full bg-background shadow-xl max-w-[750px]
        focus:outline-none"
			transition:fly={{ x: 350, duration: 300, opacity: 1 }}
		>
			<div class="flex h-full overflow-auto flex-col w-full">
				<DrawerHeader {drawer} />
				<!-- <DrawerContent  /> -->
			</div>
		</div>
	{/if}
</div>
