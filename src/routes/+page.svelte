<script>
	import Select from '../components/Select.svelte';
</script>

<h1 class="text-4xl font-bold">Hello!</h1>

<div class="w-[300px]">
	<Select
		selected="Chocolate"
		options={{
			sweet: ['Caramel', 'Chocolate', 'Strawberry', 'Cookies & Cream'],
			savory: ['Basil', 'Bacon', 'Rosemary']
		}}
	/>
</div>
