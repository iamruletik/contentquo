<script>
	import ArrowDown from './ArrowDown.svelte';

	const urls = [
		{
			label:
				'Spittfither Hello it is my game translationsspittfither hello it is my game translations o it is my game translations  is my game translations'
		},
		{ label: 'sr-Latin-RS', subItems: [], color: '#fbbf24' },
		{ label: 'Evaluation #1 (of 3)', subItems: [] }
	];
</script>

<header class="my-8 mx-12">
	<span>
		{#each urls as url, idx}
			<span key={idx} class="sub-items text-xl">
				<span
					class={idx === 1
						? 'item p-1 rounded-sm cursor-pointer whitespace-nowrap bg-amber-400'
						: ''}
				>
					{url.label}
					{#if url.subItems}<i class="fa fa-angle-down" />{/if}
				</span>
				{#if idx < urls.length - 1} / {/if}
			</span>
		{/each}
	</span>
</header>
