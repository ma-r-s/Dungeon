<script>
	import Dungeon from './dungeon/Dungeon.svelte';
	let width = 32;
	let height = 15;
</script>

<div class="flex flex-col space-y-2 m-3 items-center">
	<p class="text-2xl font-bold">Grid</p>

	<div>
		<button
			class="bg-red-300 rounded-full py-1 px-3 hover:bg-red-500"
			on:click={() => (height += 1)}>Up</button
		>
		<button
			class="bg-red-300 rounded-full py-1 px-3 hover:bg-red-500"
			on:click={() => (height -= 1)}>Down</button
		>
		<button class="bg-red-300 rounded-full py-1 px-3 hover:bg-red-500" on:click={() => (width += 1)}
			>Left</button
		>
		<button class="bg-red-300 rounded-full py-1 px-3 hover:bg-red-500" on:click={() => (width -= 1)}
			>Right</button
		>
	</div>
	<Dungeon {width} {height} />
</div>
