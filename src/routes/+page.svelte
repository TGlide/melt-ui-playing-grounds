<script lang="ts">
	import { createDialog } from '@melt-ui/svelte';
	import Drawer from '../components/Drawer.svelte';

	const drawer = createDialog();
	const { trigger } = drawer;
</script>

<button {...$trigger} use:trigger>Open</button>

<Drawer {drawer} />
