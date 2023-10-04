<script lang="ts">
	import { createDialog, type Combobox, type ComboboxStates, type ComboboxOption } from '@melt-ui/svelte';
	import Drawer from '../components/Drawer.svelte';
	import Select from '../components/Select.svelte';
	import type { Writable } from 'svelte/store';

	const drawer = createDialog();
	const {
		elements: { trigger }
	} = drawer;

	let a: Writable<ComboboxOption<unknown> | undefined>
</script>

<button {...$trigger} use:trigger>Openaa</button>

<Drawer {drawer} />

<Select bind:value={a} />