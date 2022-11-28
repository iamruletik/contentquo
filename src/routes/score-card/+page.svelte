<script>
	import ActivityLog from '../../components/ScoreCard/ActivityLog.svelte';
	import Content from '../../components/ScoreCard/Content.svelte';
	import Header from '../../components/ScoreCard/PageHeader.svelte';
	import Langs from '../../components/ScoreCard/Langs.svelte';
	import RunId from '../../components/ScoreCard/RunId.svelte';
	import Menu from '../../components/Menu.svelte';
</script>

<div class="flex">
	<Menu />
	<main>
		<Header />
		<div class="flex gap-2">
			<Langs />
			<RunId />
		</div>
		<div class="grid grid-cols-2">
			<Content />
			<ActivityLog />
		</div>

		<aside />
	</main>
</div>
