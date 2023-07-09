<script lang="ts">
	import type { CreateDialogReturn } from '@melt-ui/svelte';

	export let drawer: CreateDialogReturn;

	const { title, close } = drawer;
</script>

<div class="px-4 py-4 lg:py-3 lg:px-3 border-l-5">
	<div class="flex items-center justify-between">
		<h2
			{...$title}
			class="uppercase font-mono text-sm select-none text-green-600 font-semibold tracking-[2px] items-center flex drawer-title after:bg-green-600"
		>
			<span>data></span>
		</h2>

		<div class="ml-3 flex h-7 items-center">
			<button
				{...$close}
				use:close
				class="uppercase font-mono tracking-widest font-semibold text-sm text-foreground"
			>
				<span>Close</span>
			</button>
		</div>
	</div>
</div>
