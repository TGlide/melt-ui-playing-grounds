<script lang="ts">
	import { createCombobox, type ComboboxStates } from '@melt-ui/svelte';

	const {
		elements: { menu, input, option, label },
		states: { open, inputValue, touchedInput, selected },
		helpers: { isSelected }
	} = createCombobox({
		forceVisible: true
	});

	export const value = selected;
</script>
