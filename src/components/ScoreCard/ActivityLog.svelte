<script>
	import UiDropdown from '../UiDropdown.svelte';
	import Entity from '../Entity.svelte';
</script>

<aside class="bg-slate-400">
	<UiDropdown butontext="Export to Excel" />
	<h2>activity log</h2>
	<span class="flex items-baseline">
		<h3 class="text-lg">Manual</h3>
		<p class="text-sm">Type</p>
	</span>

	<span class="flex items-baseline">
		<h3 class="text-lg">Created at</h3>
		<p class="text-sm">14:14, 16 Nov 2022</p>
	</span>
	<Entity />
	<Entity />
	<Entity />

	<span class="flex items-baseline">
		<h3 class="text-lg">Started</h3>
		<p class="text-sm">14:14, 16 Nov 2022</p>
	</span>
	<Entity />
	<Entity />
</aside>
