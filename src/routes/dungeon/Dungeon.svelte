<script>
	export let width = 32;
	export let height = 18;
	$: col = `repeat(${width}, 1fr)`;
	$: row = `repeat(${height}, 1fr)`;
</script>

<div
	class="grid divide-x divide-y divide-gray-400"
	style="grid-template-rows: {row}; grid-template-columns: {col};"
>
	{#each Array(height).fill(0) as _, y}
		{#each Array(width).fill(0) as _, x}
			<div class="bg-gray-200 w-2 h-2" />
		{/each}
	{/each}
</div>
