<script>
	export let dashb_title = 'dashb_title';
	export let dashb_subtitle1 = 'dashb_subtitle1';
	export let dashb_subtitle2 = 'dashb_subtitle2';
	export let dashb_img = 'dashb_img';
</script>

<div class="grow  min-h-min border px-3 py-2 border-slate-200 rounded-lg">
	<div class="flex items-baseline gap-2">
		<div class="text">{dashb_title}</div>
		<div class="text-sm">{dashb_subtitle1}</div>
		<div class="text-xs">{dashb_subtitle2}</div>
	</div>
	<img class="fit-picture" src={dashb_img} alt={dashb_title} />
</div>
