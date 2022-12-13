<script>
	import ActivityLog from '../../components/ScoreCard/ActivityLog.svelte';
	import Content from '../../components/ScoreCard/Content.svelte';
	import Header from '../../components/ScoreCard/PageHeader.svelte';
	import Langs from '../../components/ScoreCard/Langs.svelte';
	import RunId from '../../components/ScoreCard/RunId.svelte';
	import Menu from '../../components/Menu.svelte';
	import MenuNavbarOLD from '../../components/MenuNavbarOLD.svelte';
	import PageTopNavbar from '../../components/PageTopNavbar.svelte';
</script>

<div class="overflow-hidden flex mb-96  w-screen">
	<div><Menu class="overflow-scroll" /></div>

	<main class="overflow-scroll">
		<!-- <MenuNavbarOLD /> -->
		<PageTopNavbar />
		<Header />
		<div class="flex gap-2">
			<Langs />
			<RunId />
		</div>
		<div class="grid grid-cols-4 gap-4 mr-14">
			<!-- не ставь сюда отступ слева даже если захочется!  -->
			<div class="col-span-3"><Content /></div>
			<div class="col-span-1"><ActivityLog /></div>
		</div>

		<aside />
	</main>
</div>
